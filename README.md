# `scapy` RTPS Experimentation

This repository sends a crafted RTPS packet to public IP addresses in the IPv4
space. The Python script utilizes a random permutation of the IPv4 address space
for efficiency and to prevent overwhelming subnets, while taking advantage of
existing packet libraries like [scapy](https://github.com/secdev/scapy).

## Prerequisites

**Python 3.10 or later** is needed to run the code in this repository.

## Setup

1. Create a virtual environment by running `python3 -m venv .venv` and activate it
   by running `. .venv/bin/activate` if you are on a Unix-based system or
   `.\.venv\Scripts\activate.bat` if you are on a Windows system.

2. Install dependencies by running `pip install -r requirements.txt`.

3. In `run_scanner.sh`, change the `$HOME_DIR` variable to point to the root
   directory of this project.

4. Run `./run_scanner.sh` to initiate the scanning process.

- If you would like to run this as a `systemctl` service, a service file is provided.
  Please update the `ExecStart` field with the correct path of the project and copy the
  file over where your system files are stored. Then run
  `sudo systemctl start scapy-rtps-experimentation.service`.
