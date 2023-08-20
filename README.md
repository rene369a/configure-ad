<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How to Deploy on-premises Active Directory within Azure Compute](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Create Domain Controller Virtual Machine, using Windows Server 2022
- Ensure Connectivity between client and Domain Controller
- Install Active Directory (AD)
- Create an Admin and Normal User Account in AD
- Join Client to your domain
- Setup Remote Desktop for non-administrative users on client computer
- Create additional users and ensure login capabilities

<h2>Deployment and Configuration Steps</h2>

<p>
<img width="1670" alt="Screenshot 2023-08-20 at 12 15 20 PM" src="https://github.com/rene369a/configure-ad/assets/142533276/379377c6-a153-480b-b9ee-7a98138e004e">
<img width="1670" alt="Screenshot 2023-08-20 at 12 16 15 PM" src="https://github.com/rene369a/configure-ad/assets/142533276/be9a7949-7647-42c7-bb9b-752b0f952efb">
</p>
<p>
- Create Domain Controller Virtual Machine, using Windows Server 2022

  - Create username and password
  - Note Resource Group created
  - Note Virtual Network (Vnet) created
  - Set Domain Controller’s NIC Private IP address to static
</p>
<p>
  <img width="1670" alt="Screenshot 2023-08-20 at 12 18 13 PM" src="https://github.com/rene369a/configure-ad/assets/142533276/9c805847-ff4f-4453-8167-60b3b0b54035">
<img width="1670" alt="Screenshot 2023-08-20 at 12 43 23 PM" src="https://github.com/rene369a/configure-ad/assets/142533276/2e12f4a4-160b-404e-be07-2ad8f258d2bb">
</p>
<br />

<p>
<img width="1670" alt="Screenshot 2023-08-20 at 12 22 30 PM" src="https://github.com/rene369a/configure-ad/assets/142533276/7e2f44c6-c0b7-4d11-b93a-9ae35760ac82">
<img width="1670" alt="Screenshot 2023-08-20 at 12 22 43 PM" src="https://github.com/rene369a/configure-ad/assets/142533276/a425a424-232f-4af0-bd9d-3cbc4843dd16">
</p>
<p>
- Create Client-1
  
  - Windows 10 VM
  - Create username and password
  - Use same Resource Group, Region and Vnet
</p>
<p>
<img width="1670" alt="Screenshot 2023-08-20 at 12 24 07 PM" src="https://github.com/rene369a/configure-ad/assets/142533276/9875fe32-99d7-472f-846c-e5baeadc966c">
</p>
<br />

<p>
<img width="1670" alt="Screenshot 2023-08-20 at 12 31 56 PM" src="https://github.com/rene369a/configure-ad/assets/142533276/c72b4af6-3745-4f5a-84f5-50a7b95c84d6">
 
<img width="1670" alt="Screenshot 2023-08-20 at 12 32 57 PM" src="https://github.com/rene369a/configure-ad/assets/142533276/2ae267f5-b862-40ee-b659-5aaddee94f3f">
</p>
<p>
- Ensure Connectivity between client and Domain Controller
  
  - Login to Client-1 with Remote Desktop
  - Ping DC-1's private IP address, use ping -t
</p>
<p>
<img width="1670" alt="Screenshot 2023-08-20 at 12 36 10 PM" src="https://github.com/rene369a/configure-ad/assets/142533276/c33e74cf-d74b-439f-94e3-506c0469dce3">
</p>
  
  - Loging to Domain Controller
  - Enable ICMPv4 on local windows firewall
  - Check Client-1 for successful ping
</p>
<p>
<img width="1670" alt="Screenshot 2023-08-20 at 12 39 28 PM" src="https://github.com/rene369a/configure-ad/assets/142533276/636dbc7d-c16f-48ae-b090-869b91cd3b96">
<img width="1670" alt="Screenshot 2023-08-20 at 12 48 02 PM" src="https://github.com/rene369a/configure-ad/assets/142533276/6e3e90d2-d7bb-445c-adbc-b16780edba49">
<img width="1670" alt="Screenshot 2023-08-20 at 12 52 45 PM" src="https://github.com/rene369a/configure-ad/assets/142533276/122439ba-940b-4bac-bded-3e12013f18ca">
</p>
<br />

<p>
  <img width="1670" alt="Screenshot 2023-08-20 at 12 59 05 PM" src="https://github.com/rene369a/configure-ad/assets/142533276/000093eb-1158-42ab-a86b-1a96a0278469">

</p>
<p>
- Install Active Directory (AD)

  - Login to DC-1 and install Active Directory Domain Services
  - Promote as a DC: Set up a new forest as mydomain.com (can be anything, just remember what it is)
  - Restart and then log back into DC-1 as user: mydomain.com\labuser
</p>
<br />

<p>
  
</p>
<p>
  
</p>
<br />

<p>
  
</p>
<p>
  
</p>
<br />
