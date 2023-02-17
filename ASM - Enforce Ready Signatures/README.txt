This is a plug-n-play script, so you shouldn't need to modify it at all. 

However, if you want to exclude specific policies, such as a Parent or Template policy, you can change the line where the FILENAME variable is created to exclude those policies like this:

FILENAME=$(curl -kvu $CREDS http://localhost/mgmt/tm/asm/policies | jq -r '.items[] | select(.name!="asm_parent") | select(.name!="asm_template") | .id')
