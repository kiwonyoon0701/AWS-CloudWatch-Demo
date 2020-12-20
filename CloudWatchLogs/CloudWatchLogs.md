```

Attach policy - CloudWatchAgentServerPolicy - to EC role


ubuntu@ip-10-100-1-108:/home/ubuntu> sudo apt-get install apache2
ubuntu@ip-10-100-1-108:/home/ubuntu> sudo service apache2 start

ubuntu@ip-10-100-1-108:/home/ubuntu> https://s3.amazonaws.com/amazoncloudwatch-agent/ubuntu/amd64/latest/amazon-cloudwatch-agent.deb

ubuntu@ip-10-100-1-108:/home/ubuntu> ls -alrt *.deb*
-rw-rw-r-- 1 ubuntu ubuntu 38406320 Nov  9 18:18 amazon-cloudwatch-agent.deb
-rw-rw-r-- 1 ubuntu ubuntu      287 Nov  9 18:18 amazon-cloudwatch-agent.deb.sig


ubuntu@ip-10-100-1-108:/home/ubuntu> wget https://s3.amazonaws.com/amazoncloudwatch-agent/assets/amazon-cloudwatch-agent.gpg

ubuntu@ip-10-100-1-108:/home/ubuntu>  gpg --import amazon-cloudwatch-agent.gpg

ubuntu@ip-10-100-1-108:/home/ubuntu>  gpg --import amazon-cloudwatch-agent.gpg
gpg: keybox '/home/ubuntu/.gnupg/pubring.kbx' created
gpg: /home/ubuntu/.gnupg/trustdb.gpg: trustdb created
gpg: key D58167303B789C72: public key "Amazon CloudWatch Agent" imported
gpg: Total number processed: 1
gpg:               imported: 1

ubuntu@ip-10-100-1-108:/home/ubuntu> gpg --fingerprint D58167303B789C72
pub   rsa2048 2017-11-14 [SC]
      9376 16F3 450B 7D80 6CBD  9725 D581 6730 3B78 9C72
uid           [ unknown] Amazon CloudWatch Agent

ubuntu@ip-10-100-1-108:/home/ubuntu> gpg --verify amazon-cloudwatch-agent.deb.sig 
gpg: assuming signed data in 'amazon-cloudwatch-agent.deb'
gpg: Signature made Thu Nov  5 01:14:09 2020 UTC
gpg:                using RSA key D58167303B789C72
gpg: Good signature from "Amazon CloudWatch Agent" [unknown]
gpg: WARNING: This key is not certified with a trusted signature!
gpg:          There is no indication that the signature belongs to the owner.
Primary key fingerprint: 9376 16F3 450B 7D80 6CBD  9725 D581 6730 3B78 9C72


ubuntu@ip-10-100-1-108:/home/ubuntu> sudo dpkg -i -E ./amazon-cloudwatch-agent.deb


```

<kbd> ![GitHub Logo](images/1.png) </kbd>