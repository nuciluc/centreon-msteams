# centreon-msteams
A Centreon plugin to send notifications to MS Teams


## Prerequisites

These perl modules need to be installed.

 - Net::Curl::Easy
 - JSON


## ToDo's
  - Write complete howto
  - Update Script --help command


## Installation

1. Place the script in /usr/lib64/nagios/plugins
2. `chmod +x /usr/lib64/nagios/plugins/notify-msteams-*.pl`
3. Configure commands on Centreon (using Resource $USER1$)


## Usage

Examples:

Command Name: host-notify-by-msteams  
Command Type: Notification  
Command Line: $USER1$/notify-msteams-host.pl --wh='https://outlook.office.com/webhook/CHANGEME' --nt='$NOTIFICATIONTYPE$' --hn='$HOSTNAME$' --hs='$HOSTSTATE$' --ha='$HOSTADDRESS$' --ho='$HOSTOUTPUT$' --dt='$SHORTDATETIME$'  
Enable shell: Yes  

Command Name: service-notify-by-msteams  
Command Type: Notification  
Command Line: $USER1$/notify-msteams-service.pl --wh='https://outlook.office.com/webhook/CHANGEME' --nt='$NOTIFICATIONTYPE$' --sd='$SERVICEDESC$' --hn='$HOSTALIAS$' --ha='$HOSTADDRESS$' --ss='$SERVICESTATE$' --dt='$SHORTDATETIME$' --so='$SERVICEOUTPUT$'  
Enable shell: Yes  


# Reference

https://docs.microsoft.com/en-us/outlook/actionable-messages/message-card-reference
