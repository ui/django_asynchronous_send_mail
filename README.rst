
INSTALLATION
============

Put django_asynchronous_send_mail in your Python path.



USAGE
=====


    try:
        from django_asynchronous_send_mail import send_mail
    except:
        from django.core.mail import send_mail
        
The rest is the same as Django's normal send_mail(), in fact, if your project already uses Django's built in send_mail(), you don't need to change anything :)


Example::    
    
    send_mail('Subject here', 'Here is the message.', 'from@example.com', ['to@example.com'], fail_silently=False)
    
If you want to send HTML email::

    send_mail('Subject here', 'Here is the message.', 'from@example.com', ['to@example.com'], fail_silently=False, html = '<HTML_TEXT_HERE>')
