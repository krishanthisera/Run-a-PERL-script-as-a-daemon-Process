# Run-a-PERL-as-a-daemon-Process

logger.pl is a Perl program which is required to run as daemon process. 

1.	Check your PERL version.

      which Perl 
      
2.	Run CPAN console

      cpan 
      

3.	Install relevant packages

      install Proc::Daemon
      
      install Net::Finger [If you going to run that particular Perl script using crontab]
      
4.	Refer the logger.pl file to source code for the Perl daemon process implementation. 
