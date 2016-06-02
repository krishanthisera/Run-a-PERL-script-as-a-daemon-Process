# Run-a-PERL-as-a-daemon-Process

logger.pl is a Perl program which is required to run as daemon process. 

1.	Check your PERL version.

                  [root@localhost ~]# which perl
                  /usr/bin/perl
 
      
2.	Run CPAN console

                  [root@localhost ~]# cpan
                  Terminal does not support AddHistory.

                  cpan shell -- CPAN exploration and modules installation (v1.9800)
                  Enter 'h' for help.

                   cpan[1]>
 
      

3.	Install relevant packages

                  cpan[1]> install Proc::Daemon
      
                  cpan[2]> install Net::Finger [If you going to run that particular Perl script using crontab]
       
4.	Refer the logger.pl file to source code for the Perl daemon process implementation. 

  !!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!BEWARE!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!!

when you add Perl scripts to crontab those files. Because when crontab running it WILL NOT check the 
existence of the particular Perl (or whatever) process so your process will be replicated and finally 
				you will lose the CPU and memory resources. 
 ===========================================================================================
       Reffer to avoid replication issue
       https://github.com/krishanthisera/RUN-Perl-Process-on-the-crontab-Without-relication-
 ===========================================================================================
