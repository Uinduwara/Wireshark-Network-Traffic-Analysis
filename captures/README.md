# Network Traffic Sample Captures

This folder documents the public sample packet captures used in Cybersecurity Project 02 – Network Traffic Analysis Using Wireshark.

The captures were obtained from Wireshark's publicly available training resources.

## Capture Files

| File | Analysis |
|---|---|
| `dns.cap` | DNS requests, responses, transaction IDs, and response times |
| `3-way-handshake.pcap` | TCP SYN, SYN-ACK, and ACK packets |
| `http.cap` | HTTP GET requests and server responses |
| `dump.pcapng` | TLS handshakes, encrypted traffic, and network statistics |

## Sources

- [Wireshark Sample Captures](https://wiki.wireshark.org/SampleCaptures)
- [Wireshark TCP Three-Way Handshake](https://wiki.wireshark.org/TCP_3_way_handshaking/)
- [Wireshark TLS](https://wiki.wireshark.org/TLS/)

## How to Reproduce the Analysis

1. Download the relevant sample capture from the official source.
2. Open the file in Wireshark.
3. Apply the relevant display filter.
4. Select the matching packets.
5. Expand the protocol details.
6. Compare your observations with the investigation report.

## Wireshark Display Filters

| Purpose | Filter |
|---|---|
| DNS traffic | `dns` |
| UDP traffic | `udp` |
| TCP traffic | `tcp` |
| HTTP traffic | `http` |
| TLS traffic | `tls` |
| TLS Client Hello | `tls.handshake.type == 1` |
| TLS Server Hello | `tls.handshake.type == 2` |
| TLS Application Data in Stream 1 | `tcp.stream == 1 && tls.record.content_type == 23` |

## Notes

These capture files are intended for educational protocol analysis.

The datasets represent separate capture sessions and should not be interpreted as one continuous network investigation.

The original files are available from Wireshark's public resources and do not need to be redistributed in this repository.