*This project has been as part of the 42 curriculum by fgoncal2.*

# Born2BeRoot

## Description

**Born2beroot** is a system administration project aimed at setting up and securing a Linux server inside a virtual machine.

The project introduces fundamental concepts of:
- Virtualization
- Linux system administration
- User and group management
- Disk partitioning
- Security policies
- Network and firewall configuration
- Services monitoring

## Project Design & Technical Choices

### Operating System Choice: Debian (Linux)

I chose Debian as the operating system for this project.

Reasons for choosing Debian:

- Stable and well-documented
- Widely used in server environments
- Large community support
- Simpler learning curve compared to enterprise-focused 	distributions

### Other Choices and comparissons

#### Debian vs Rocky Linux

- Debian
  - Community-driven
  - Excellent extensive documentation
  - Great for learning
  - Very stable
- Rocky Linux
  - Enterprise-oriented (RHEL-compatible)
  - Strong for production servers
  - More complex

#### AppArmor vs SELinux

- AppArmor
  - Easier to understand and configure
  - Profile-based path restrictions
  - Enabled by default on debian
- SELinux
  - More powerful
  - Steeper learning curve
  - Common in enterprise systems

#### UFW vs firewalld

- UFW
  - Simple and readable rule syntax
  - Straightforward configuration
  - Best for small servers and learning
- Firewalld
  - more complex
  - zone-based and dynamic

#### Virtualbox vs UTM

- VirtualBox
  - cross-platform
  - beginner-friendly
  - well documented
- UTM
  - macOS foccused
  - simple UI but more advanced overall

---

## Instructions

### Virtual Machine Setup

1. Create a new virtual machine using **VirtualBox**
2. Install **Debian (minimal installation)**
3. Configure:
   - Hostname
   - Users and groups
   - Disk partitioning with LVM
   - Network settings

---

### System Configuration

- Enable and configure UFW firewall
- Configure SSH on port `4242`
- Disable root SSH login
- Enable AppArmor
- Configure password policy:
  - Minimum length
  - Expiration rules
  - Complexity requirements

---

### Monitoring Script

A monitoring script is configured using `cron` to periodically display:
- System architecture
- CPU and RAM usage
- Disk usage
- Network activity
- Logged-in users
- Sudo commands count

---

## Resources

- debian documentation: https://www.debian.org/doc/
- `man sudo`, `man ssh`, `man ufw`
- AppArmor Documentation: https://gitlab.com/apparmor/apparmor/-/wikis/home


### Ai Usage disclosure

Ai tools were used for:
- Clarifying Linux concepts
- Reviewing documentation
- Structuring this README document
