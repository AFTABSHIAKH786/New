4h0j2gkp8s4x.cloud.wazuh.com
 
Invoke-WebRequest -Uri https://packages.wazuh.com/4.x/windows/wazuh-agent-4.10.1-1.msi -OutFile $env:tmp\wazuh-agent; msiexec.exe /i $env:tmp\wazuh-agent /q WAZUH_MANAGER='4h0j2gkp8s4x.cloud.wazuh.com' WAZUH_REGISTRATION_PASSWORD='mNmLK1OGzQTOzXvkcHSEkySN7x8Rf74E' WAZUH_AGENT_NAME='aftab'
 
NET START WazuhSvc
 
