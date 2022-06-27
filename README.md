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


# Enable JIT access when trying to RDP
- This adds more restrictions and prevents just anyone from RDP into the virtual machine

<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/175852969-b008961c-5735-488c-9e92-2dd962be2b41.png" height="90%" width="90%" alt="JIT Access"/>

<p/>

# Request JIT access from your IP
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/175853023-8f348ad2-7850-4011-9e21-1a661d6e4431.png" height="90%" width="90%" alt="JIT Access"/>

<p/>

# Network rules will be created 
- One rule will deny anyone IP from RDP into the JIT virtual machine - Priority 1000
- The other rule will create an allow rule for your machine's public IP to access JITvm's IP - Priority 101
- Microsoft Defender will create these rules
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/175853269-118a6c8c-f654-43f2-9be4-20c17e3e2837.png" height="150%" width="150%" alt="JIT Access"/>

<p/>



# JIT VM Access - Custom Role
- Custom Roles can be created specifically for JIT access.
- Within the red box are the JSON code that will create the permissions for the JIT role
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/175986992-b323e195-2a72-44c7-a4d4-1091c1833ae3.png" height="90%" width="90%" alt="JIT Access"/>

<p/>

# Assign the custom JustInTime Access role to a user
<p align="center">
  
<img src="https://user-images.githubusercontent.com/104326475/175987400-44883bcc-5dd3-4a6a-9f01-dcecbf0383e8.png" height="90%" width="90%" alt="JIT Access"/>

<p/>


