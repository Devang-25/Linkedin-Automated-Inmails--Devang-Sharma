LinkedInMailing
===============
Sends email to any Recruiter/Talent Acquisitionist with a copy of your resume and a small message from your LinkedIn network.
It takes in your contact list from LinkedIn in .csv format, reusme copy, and the message in a text file.

```
    usage: mail.py [-h] [-ex old_file] sender_list attach_path text_body
      
    Sends email with attachment to multiple recipients.
      
    positional arguments:
        sender_list         Path to the text file containing list of senders
        attach_path         Path to the attachment file
        text_body           Path to the text file containing email message
        
    optional arguments:
        -h, --help          show this help message and exit
        -ex old_file, --exclude old_file
                            Compare new contact file with old and send the mail to
                            new ones only
```

- Get your contact list from here: https://www.linkedin.com/people/export-settings
- The message should replace the Recruiter's name tag with {Name}, Company's name tag with {Company}, and your name as {User}
- Example: mail.py /path/to/contacts.csv /path/to/myResume.pdf /path/to/myMessage.txt
- The -ex flag takes in an old .csv file that you may have used earlier and compares it with the new one to just send the email to any new connections you have

**Update:** with the new security changes from Google, you'd have to turn on the less secure apps options from your account to run this script. Turn it on from, https://www.google.com/settings/security/lesssecureapps.
