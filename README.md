# CreateAWSIAMUsers

Quickwrapper for creating users on the fly. 

### CreateAWSCLIUsers: Create users on the fly with credentials. ###
   
[EXAMPLE-A]: scriptname -p <amazon_profile> -P S0m3L@m3P@Ssw0rD - u someusernamehere -g DevelopmentUsers

[EXAMPLE-B]: scriptname -p <amazon_profile> -P 'S0m3L@m3P@Ssw0rD' - u someusernamehere -g 'DevUser Individual-MFA TestUser'
          
### REQUIREMENTS:
 
This script requires only three arguments -p, -u and -P, and requires the user to have setup aws profiles setup in order to use this tool.
 
### Arguments 

[REQUIRED ARGUMENTS]:

   -P) [initialPassword] [STRING] This option refers to the initial user password. This supports single quoted strings for funky passwords that would otherwise glob.
   
   -p) [profile] [STRING] This option refers to the profile to be used for AWS. This should exist in /home/jonathanwindham/.aws/credentials.
   
   -u  [user] [STRING] This is the username that you are creating.
   
   -g  [groups] [STRING || IFS seperated string] This function is serviced via 'for'.  You can provide an item, like groupname1, or an IFS seperated and quoted string for multiple groups. 'groupname1 groupname2'
 
 
[OPTIONAL ARGUMENTS]:
   -h) [HELP] [takes no arguements] Print this dialog to the screen.
