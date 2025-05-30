## Task: Firewall Configuration using UFW on Kali Linux

This task involves configuring firewall rules using **UFW (Uncomplicated Firewall)** on Kali Linux to control inbound network traffic.

### Objectives:
- Check and enable UFW if it is inactive.
- List existing firewall rules.
- Block inbound traffic on port **23** (Telnet) to enhance security.
- Verify the blocking rule by testing a Telnet connection.
- Allow SSH traffic on port **22** for secure remote access.
- Remove the test block rule to restore the firewall to its original state.

### Commands Used:
```bash
# Check UFW status
sudo ufw status

# Enable UFW if inactive
sudo ufw enable

# List firewall rules with numbering
sudo ufw status numbered

# Block inbound traffic on port 23 (Telnet)
sudo ufw deny 23

# Install telnet client for testing
sudo apt install telnet

# Test connection to port 23 (should be refused)
telnet localhost 23

# Allow inbound SSH traffic on port 22
sudo ufw allow 22

# Delete the block rule for port 23 (replace [num] with actual rule number)
sudo ufw delete [num]

# Final firewall status check
sudo ufw status
