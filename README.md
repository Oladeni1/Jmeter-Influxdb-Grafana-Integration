## Jmeter-Influxdb-Grafana-Integration
How to perfom Jmeter-Influxdb-Grafana-Integration

## To opening influxdb windows amd64
open the complete path of the influxdb with powershell > e.g - C:\Program Files\Influxdb\influxdb\influxdb2_windows_amd64

Run > .\influxd.exe  

## Navigate to browser and visit > 127.0.0.1:8086

Setup your influxdb account or login - Oladeni1/1Latunde

influxdb token: NE66mSeadfM5WC8PpoU8lFoK1lXmjWWIif4jEpDNaaiTnQtztD44YoIcfROQvGaqOH2w2KIsqvQausUpvK7uFA==


## To opening influx cli client windows:
 
Go to the influx cli client windows path,> e.g - C:\InfluxDB\influxDB_Cli_windows

Run > .\influx.exe v1 dbrp list --org GCML --token NE66mSeadfM5WC8PpoU8lFoK1lXmjWWIif4jEpDNaaiTnQtztD44YoIcfROQvGaqOH2w2KIsqvQausUpvK7uFA==

## To create database within your organisation and specific bucket, run below command with input of ids::

Run > .\influx.exe v1 dbrp create --org-id <orgID> --bucket-id <bucketID> --db <yourDatabaseName> --rp <retensionPolicyName> --token <tokenID>

For example:
.\influx.exe v1 dbrp create --org-id 186bd74894f2557d --bucket-id f8f6049989c8af86 --db Jmeter-db --rp Jmeterdb-rp --token NE66mSeadfM5WC8PpoU8lFoK1lXmjWWIif4jEpDNaaiTnQtztD44YoIcfROQvGaqOH2w2KIsqvQausUpvK7uFA==

## My current influx database details:

influxDBOrg: GCML
influxBucket: jmeter
influxDBDatabase: Jmeter-db
influxDBUser: jmeteruser
influxDBPassword: jmeterpwd123


## To Create user + pwd for database access, run below command with input of ids: 

Run > .\influx.exe v1 auth create --read-bucket <bucketID> --write-bucket <bucketID> --username <demouser> --password <demopwd123> --token <yourtokenID> --org-id <orgID> 

For example: 
.\influx.exe v1 auth create --read-bucket f8f6049989c8af86 --write-bucket f8f6049989c8af86 --username jmeteruser --password jmeterpwd123 --token NE66mSeadfM5WC8PpoU8lFoK1lXmjWWIif4jEpDNaaiTnQtztD44YoIcfROQvGaqOH2w2KIsqvQausUpvK7uFA== --org-id 186bd74894f2557d 

output after execution:

ID                      Description     Username        v2 User Name    v2 User ID              Permissions
0b83b116914a5000                        jmeteruser      Oladeni1        0b7dde6b6f12d000        [read:orgs/186bd74894f2557d/buckets/f8f6049989c8af86 write:orgs/186bd74894f2557d/buckets/f8f6049989c8af86]


## My Grafana: Org - GCML
https://olatundeoladeni1976.grafana.net/login

## To open grafana from the path with powershell,

Go to the path of your grafana bin folder e.g - C:\Grafana\grafana-10.0.2\bin

Run > grafana.exe

Run > grafana-server.exe

Navigate to browser and visit > 127.0.0.1:8087

or

visit site > https://olatundeoladeni1976.grafana.net/login

Setup your influxdb account or login - admin/admin

## To create dashboard:-

Go to dashboard and create one from import:

import via Grafana.com > use ID = 1152 (Click on the Load button), select your datasource name from dropdown and click import. 

The dashboard will be created/displayed.

Apache JMeter Dashboard using Core InfluxdbBackendListenerClient json location - https://grafana.com/grafana/dashboards/5496

or

Apache JMeter Dashboard using JMeterLoadTest json location - https://grafana.com/grafana/dashboards/1152-jmeter-load-test/
