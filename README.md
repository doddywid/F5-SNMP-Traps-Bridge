# F5-SNMP-Traps-Bridge
Provide bridge for SNMP Traps sent from multiple BIGIP devices to 3rd party Traps Manager
Refer to https://github.com/doddywid/F5-SNMP-MIB/ for brief explanation of F5 SNMP MIB & Traps structure

This repository is to provide solution for problems below  
- provide concentrator and single source for SNMP Trap manager to collect traps from multiple BIGIP devices 
- provide API for query recent time traps (which may be converted to CSV) 
- conversion of active traps data to CSV format is not done yet

Highlevel step:
1. Setup ELK
2. Setup Nginx for ELK (optional)
3. Enable IPv4 forwarding
4. Configure IPtables rules (please refer to /Config/IPtables-config.txt)
5. Configure logstash to ingest snmptrap and output to elasticsearch
6. Query API (please refer to /Config/Logstash-query-API.txt)
7. Convert JSON to CSV (to be done, can be shell script or ouput from logstash)
