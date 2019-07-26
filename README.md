# DCV-Basic-SSL-Decrypt-Policy
This skillet creates a basic ssl decryption policy that installs a self-signed certificate and a decryption policy that decrypts high-risk categories and the eicar antivirus test site.

This skillet pushes a self-signed certificate to a firewall, configures it as the forward-trust-certificate and creates a decryption policy and profile.  It also creates a custom URL category for the *.eicar.org website and enables high-risk and this custom category for decryption.  This skillet is meant mostly for POC or demonstration purposes.  Production environments are likely to leverage an internal PKI environment to perform decryption instead of using a self-signed certificate.

To use the skillet, select the VSYS (default vsys1) and deploy to the firewall.  If testing decryption with AntiVirus, browse to the eicar test virus site through the firewall and download the test file using https.  If you have not imported the certificate in the system’s local trusted certificate store, you will receive a certificate error.  The download will be blocked.  The other high-risk URL categories that are part of the decryption rule are:

•	Adult

•	Command-and-Control

•	Content-Delivery-Networks

•	Copyright-Infringement

•	Dynamic-DNS

•	Gambling

•	Hacking

•	High-Risk

•	Malware

•	Parked

•	Peer-to-Peer

•	Proxy-Avoidance-and-Anonymizers

•	Shareware-and-Freeware

•	Social-Networking

•	Unknown

Support Policy
The code and templates in the repo are released under an as-is, best effort, support policy. These scripts should be seen as community supported and Palo Alto Networks will contribute our expertise as and when possible. We do not provide technical support or help in using or troubleshooting the components of the project through our normal support options such as Palo Alto Networks support teams, or ASC (Authorized Support Centers) partners and backline support options. The underlying product used (the VM-Series firewall) by the scripts or templates are still supported, but the support is only for the product functionality and not for help in deploying or using the template or script itself. Unless explicitly tagged, all projects or work posted in our GitHub repository (at https://github.com/PaloAltoNetworks) or sites other than our official Downloads page on https://support.paloaltonetworks.com are provided under the best effort policy.
