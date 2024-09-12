https://youtrack.jetbrains.com/issue/IJPL-71010

The file is recognized as a Compose one in the following cases (without version key presence, which is deprecated now):

if the name contains compose and the services top-level element is presented;
if the services top-level element is presented along with some another top-level element (networks, volumes, configs, etc).