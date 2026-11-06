# daygauge sleep midpoint

Calculate a sleep midpoint from manually supplied sleep onset and wake times using [daygauge's public method](https://daygauge.com/guides/sleep-midpoint-calculator/). The skill handles midnight, invalid times and ambiguous intervals. It does not read Apple Health, connect to the daygauge app or interpret a medical condition.

Import this Agent Plugins v1 package into Hermes and invoke `daygauge-agent-plugin:daygauge-sleep-midpoint`. The skill requests only manually supplied times; Hermes and the user's configured model service process those values. The package contains no executable code, network client, install script, credential store, background process or telemetry.

MIT covers this package; product names and service access retain their separate terms.
