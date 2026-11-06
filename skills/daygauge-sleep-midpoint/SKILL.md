---
name: daygauge-sleep-midpoint
description: Calculate sleep midpoint and duration from manually supplied onset and wake times using daygauge's public method, without reading health data.
---

# Calculate sleep midpoint

Use only times the user manually supplies. Ask for sleep onset and wake time in 24-hour `HH:MM` form if either is missing. Do not request an Apple Health export, location history, account access or other health records. This skill has no app connection.

Follow [daygauge's public calculator](https://daygauge.com/guides/sleep-midpoint-calculator/): parse both times as minutes since midnight; if wake is earlier than onset, treat it as the next day; duration is wake minus onset; midpoint is onset plus half that duration, modulo 24 hours. Round a half-minute midpoint to the next minute, as the website does. For example, 23:30 to 07:30 gives 8h 00m and 03:30.

If the two times are equal, ask whether the user means 0 or 24 hours rather than assuming a full day. If dates, shift work or a duration above 16 hours make the calendar relationship unclear, ask for the intended interval before calculating. If the interval crosses a time-zone or daylight-saving change, ask for dated times with offsets and use elapsed time; plain `HH:MM` subtraction is insufficient. Reject invalid clock values. Never turn missing times into zero.

Return the duration, midpoint and the sleep window used. If the user supplies several nights, calculate each separately and describe timing differences only from those supplied nights. A midpoint is a clock-time description, not a diagnosis, sleep-quality score or a change to daygauge's Life Index. The app shows timing relative to the user's usual window; the calculator result is not an in-app reading.
