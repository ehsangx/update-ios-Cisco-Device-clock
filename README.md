# update-ios-Cisco-Device-clock
برای شرایطی که OS بروزرسانی timezone  را دریافت نکند و DST را نتوان به صورت دستی  فعال یا غیر فعال کرد بهترین گزینه یک NTP سرور غیر واقعی است مانند روتر و یا سوئیچ سیسکو 
برای این منظور میبایست روتر را با دستور ntp master  به حالت NTP سرور درآوریم
و ساعت را به صورت دستی روی آن تنظیم کرد
برای بروزرسانی ساعت خودکار نیاز به یک اسکریپت است که به طور مثال ساعت را با تغییر یک  ساعت روی تجهیز سیسکو اعمال کنه





.
The best option for situations where the OS does not receive timezone updates and DST cannot be manually enabled or disabled is to use a non-real NTP server such as a Cisco router or switch. 
To do this, you need to set up the router as an NTP server using the "ntp master" command and manually set the time on it. To update the time automatically, you will need a script that, for example, changes the time by one hour on the Cisco device.


Install & run :

1- pip install netmiko

2- python3 ios-set-clock.py

