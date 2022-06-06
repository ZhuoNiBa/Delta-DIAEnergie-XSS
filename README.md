# Delta-DIAEnergie-XSS

## Delta Electronics DIAEnergie 1.08.00 Exists XSS Vulnerability
### Vulnerability Introduction
DIAEnergie in the "System Settings"--"IoT Hub Settings" menu bar, when creating a new "shift setting" (url is "/api/DiaSettings/PutIoTHubSetting"), perform xss test on the "name" field, directly When the page is tested, the system will prompt "A potentially dangerous Request.Form value detected from the client (name="123<script>alert(123)</script>")", but in fact the xss script has Submitted successfully.

download link：https://downloadcenter.delta-china.com.cn/downloadCenterCounter.aspx?DID=39971&DocPath=1&hl=zh-CN
### Vulnerability verification process
1. In the menu "System Settings" - "IoT Hub Settings", submit "<script>alert(123)</script>" in the name field when creating a new "Shift Settings"

