4h0j2gkp8s4x.cloud.wazuh.com
 
Invoke-WebRequest -Uri https://packages.wazuh.com/4.x/windows/wazuh-agent-4.10.1-1.msi -OutFile $env:tmp\wazuh-agent; msiexec.exe /i $env:tmp\wazuh-agent /q WAZUH_MANAGER='4h0j2gkp8s4x.cloud.wazuh.com' WAZUH_REGISTRATION_PASSWORD='mNmLK1OGzQTOzXvkcHSEkySN7x8Rf74E' WAZUH_AGENT_NAME='aftab'
 
NET START WazuhSvc
 




wget https://packages.wazuh.com/4.x/apt/pool/main/w/wazuh-agent/wazuh-agent_4.10.1-1_amd64.deb && sudo WAZUH_MANAGER='4h0j2gkp8s4x.cloud.wazuh.com' WAZUH_REGISTRATION_PASSWORD=$'mNmLK1OGzQTOzXvkcHSEkySN7x8Rf74E' WAZUH_AGENT_GROUP='default' WAZUH_AGENT_NAME='aftab' dpkg -i ./wazuh-agent_4.10.1-1_amd64.deb
 
sudo systemctl daemon-reload sudo systemctl enable wazuh-agent sudo systemctl start wazuh-agent
 
