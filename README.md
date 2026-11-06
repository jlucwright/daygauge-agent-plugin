# daygauge sleep midpoint

Calculate a sleep midpoint from manually supplied sleep onset and wake times using [daygauge's public method](https://daygauge.com/guides/sleep-midpoint-calculator/). The skill handles midnight, invalid times and ambiguous intervals. It does not read Apple Health, connect to the daygauge app or interpret a medical condition.

Import this Agent Plugins v1 package into Hermes and invoke `daygauge-agent-plugin:daygauge-sleep-midpoint`. Only the times the user supplies are processed by their configured Hermes and model service. The package has no executable code, install scripts, network calls, file reads, credentials, background processes or telemetry.

MIT covers this package; product names and service access retain their separate terms.
