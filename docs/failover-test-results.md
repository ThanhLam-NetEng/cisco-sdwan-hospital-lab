# Failover Test Results

## Test Date: April 17, 2026

## Environment

- Platform : Cisco dCloud APJ (Singapore)
- SD-WAN : Catalyst 20.18.2.1
- Devices : Edge1 (C8000v) - Site 1

## Test Scenario

Manual shutdown of MPLS interface on CML node
to simulate real-world link failure.

## Timeline

| Time     | Event                           |
| -------- | ------------------------------- |
| 01:16 AM | MPLS shutdown executed          |
| 01:16 AM | Control Connection State Change |
| 01:17 AM | Edge1 FIB table update begins   |
| 01:19 AM | Full convergence achieved       |

## Results

- Convergence Time : ~3 minutes
- Manual Intervention : Zero
- Traffic Continuity : Automatic switchover
- Recovery Path : MPLS → biz-internet

## Validation Method

vManage Events Log with exact timestamps
