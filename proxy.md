#======
Work proxy:
Powershell:
$browser = New-Object System.Net.WebClient
$browser.Proxy.Credentials =[System.Net.CredentialCache]::DefaultNetworkCredentials
Invoke-WebRequest https://www.google.com
Reset by:
netsh winhttp show proxy
netsh winhttp reset proxy
Git:
git config --global https.proxy http://swgscanning.ttcg.com:8080
git config --global http.proxy http://swgscanning.ttcg.com:8080
No Proxy:
git config --global --unset https.proxy
git config --global --unset http.proxy
Show Proxy details:
git config --global --get-regexp http.*