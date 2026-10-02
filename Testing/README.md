# Testing
Tests: Ping between VLANs via R1, DHCP clients get IP, NAT ping 8.8.8.8 from all VLANs, Server accessible from all VLANs.

| Test | Source | Destination | Command | Expected | Actual | Status |
|------|--------|-------------|---------|----------|--------|--------|
| 1 | Staff 10.25.10.11 | 10.25.10.1 | ping | Success | Success | PASS ✅ |
| 2 | Staff 10.25.10.11 | 10.25.30.10 | ping | Success | Success | PASS ✅ |
| 3 | Guest 10.25.20.11 | 10.25.10.1 | ping | Fail | Timed Out | PASS ✅ |
| 4 | Guest 10.25.20.11 | 10.25.30.10 | ping | Fail | Timed Out | PASS ✅ |
| 5 | Guest 10.25.20.11 | 8.8.8.8 | ping | Success | Success | PASS ✅ |
| 6 | Any PC | DHCP | ipconfig | .11+ | .11 | PASS ✅ |

**ACL 100 Proof:** Guest isolation working. Counters on deny increase.
**NAT Proof:** Ping 8.8.8.8 works after NAT.
