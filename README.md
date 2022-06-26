# Just-In-Time-Access

# What is JIT access?
- This feature is used when admins need to gain access to a VM.
- The NSG may have a rule that allows traffic on port 3389 (RDP). 
- The JIT will work with NSG. JIT will add a rule to the NSG and allow access only when required.



# Within Defender - JIT VM access
- Admins can control the duration for which a user can connect to an Azure VM
- Users will need to request access from their machines's public IP address
- Once access is request, Microsoft Defender will create a inbound allow rule for your machine's IP.
- That rule will trump the RDP inbound rule.

