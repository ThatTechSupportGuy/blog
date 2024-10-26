---
layout: post
title: Sql Developer on Linux
categories: technology
---

### Installing sql developer on Linux.
1. Go to oracle OTN site and download the software. Select other platforms as the software choice.
2. Extract the .zip downloaded to a folder like sqldeveloper.
3. sudo mv sqldeveloper /opt/ ( Move the folder to opt directory)
4. chmod +x /opt /sqldeveloper/ sqldeveloper.sh ( make the script file a executable)
5. gedit sqldeveloper.sh
Comment out the code in the file and replace that with :
unset -v GNOME_DESKTOP_SESSION_ID cd /opt/sqldeveloper/sqldeveloper/bin && bash sqldeveloper $*
6. Create a softlink for the executable file
sudo ln -s /opt/sqldeveloper/sqldeveloper.sh /usr/local/bin/sqldev
Here the link name is sqldev
7. Ctrl+alt+t to bring up the terminal and type sqldev and click enter
8. When the application starts it's gonna ask for Java Home ;
usually it's under/usr/lib/jvm/java-8-oracle (a path like this)
9. If Java doesnt exist, open up another terminal and install the same via these commands:
* sudo apt-add-repository ppa:webupd8team/java * sudo apt-get update * sudo apt-get install oracle-java8-installer
10. Provide the path and watch sql developer load.
11. There are additional jdbc drivers for mysql etc on OTN.
Copy the extracted file to sql developer folder.
go to sqldeveloper>tools>preferences> datbases> third party> and provide the path of the downloaded folder upto the path where .jar file exists.