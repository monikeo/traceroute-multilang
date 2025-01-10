# traceroute-multilang
A comprehensive traceroute implementation in multiple programming languages (Python, Rust, etc.), complete with tutorials, explanations, and colorful CLI features. Learn about traceroute principles, protocols (ICMP, UDP, TCP), and how to build modern, maintainable networking tools.

## Introduction

Traceroute is a tool used to map the path packets take to reach a destination on a network. By incrementing the Time-To-Live (TTL) value of packets, traceroute identifies each hop along the route and measures the latency at each step.

This project explores:
- The principles and protocols behind traceroute (ICMP, UDP, TCP).
- Implementing traceroute in various programming languages.
- Designing a modern, modular, and user-friendly traceroute tool.

## How Traceroute Works

Traceroute operates by sending packets with progressively increasing TTL values. Each router along the path decrements the TTL and descards the packet when TTL reaches 0, sending back an ICMP Time Exceeded message. This allows the tool to:
- Discover the IP addresses of intermediate router.
- Measure round-trip times (RTTs) for each hop.

Traceroute can use different protocols, such as:
- **ICMP**: Sends ICMP Echo Request packets.
- **UDP**: Sends UDP packets to high-numbered ports.
- **TCP**: Sends TCP SYN packets, useful for traversing firewalls.


# Getting Started

### Clone the Repositoty

```bash
# Clone this repository
$ git clone https://github.com/monikeo/traceroute-multilang.git
$ cd traceroute-multilang
```

### Dependencies

Dependencies vary by language. Refer to the tutorial.md in each language
directory for detailed instructions.

**Example: Python**
```bash
#Navigate to the Python implementation directory
$cd implementation/python

# Install dependencies
$ pip Install -r requirements.txt
```

**Example: Rust**
```bash
#Navigate to the Rust implementation directory
$ cd implementation/rust

# Build the project
$ cargo build
```

### Running Implementations

**Example: Python**
```bash
$ python traceroute.py camtech.edu.kh --protocol UDP
```

**Example: Rust**
```bash
$ cargo run -- camtech.edu.kh --protocol UDP
```


