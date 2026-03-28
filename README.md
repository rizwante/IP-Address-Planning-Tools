# IP-Address-Planning-Tools
A comprehensive, browser-based network utility for IPv4/IPv6 subnetting, VLSM planning, IP summarization, and address space management.

IP Address Planning Tools 🌐

A comprehensive, professional-grade browser utility designed for network engineers, system administrators, and IT students. This tool provides robust calculations, visualizations, and planning utilities for both IPv4 and massive 128-bit IPv6 address spaces.

🚀 Live Demo

Launch IP Address Planning Tools
(Note: Replace with your actual GitHub Pages URL after deployment)

🌟 General Features

Seamless IPv4 & IPv6 Support: Every module natively supports both IP versions.

"Copy for Excel": Every table and output can be copied directly to your clipboard in a tab-separated format that pastes perfectly into Microsoft Excel or Google Sheets.

Local History Tracking: Your recent inputs are saved locally in your browser. Click on history tags to quickly reload previous queries.

Dark Mode: High-contrast dark theme support for low-light environments.

🛠️ Key Modules

1. IPv4/IPv6 Calculator

The starting point for analyzing individual IP addresses and their network boundaries.

Function: Determines network address, broadcast, wildcard mask, and usable host ranges.

Magic Paste: Paste IPs with CIDR notation (e.g., 192.168.1.50/26) to auto-split fields.

Full Range Export: Generate and copy every single usable IP in a given subnet.

2. Subnet Generator

Carve large networks into multiple equally-sized smaller networks.

Major Network Mode: Split a parent block (e.g., /8) into specific targets (e.g., /16).

IP Range Mode: Find all valid subnets that fit perfectly between two specific IP addresses.

3. VLSM & Visual Map

A visual IP planner designed for high-efficiency network design using Variable Length Subnet Masking.

Allocation: Define requirements by host count or CIDR.

Binary Treemap: A mathematical visualization showing how the parent block is split on bit boundaries.

Linear Proportion Bar: See exactly how much space each subnet occupies relative to the whole.

4. IP Summarization (Supernetting)

Consolidate a list of disparate IPs or ranges into the tightest possible routing blocks.

Optimization: Ideal for building ACLs or optimizing routing tables.

Auto-Sizing: Automatically calculates the absolute tightest CIDR blocks if no target mask is provided.

5. Free Space Finder

A powerful IPAM utility to audit existing networks and locate contiguous gaps.

Space Mapping: Paste used prefixes to see a map of the entire parent block.

Gap Detection: Precisely identifies the CIDR blocks available in "Free" gaps.

6. MAC & EUI-64 Utility

MAC Conversion: Formats MACs for Cisco (dots), Windows (hyphens), or Unix (colons).

IPv6 Generation: Automatically performs "bit-flipping" and FFFE injection to generate EUI-64 interface IDs.

📖 Practical Examples

VLSM Planning

Scenario: Office setup with 192.168.1.0/24. Need HR (60 devices), IT (25 devices), and 3 Point-to-Point links.

Result: The tool allocates /26 for HR, /27 for IT, and three /30s for links, ensuring no overlaps and zero wasted space.

Space Recovery

Input: Parent 172.16.0.0/12, Used 172.16.0.0/16.

Result: Identifies three perfectly aligned free blocks: 172.17.0.0/16, 172.18.0.0/15, and 172.20.0.0/14.

👨‍💻 Developer & Credits

Rizwan Ghani

LinkedIn: linkedin.com/in/rizwanghani

Project Goal: To provide a free, high-performance alternative to complex IPAM software for day-to-day engineering tasks.

Developed with React and Tailwind CSS. All calculations are performed client-side using BigInt for 100% accuracy.
