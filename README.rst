=============================
django-asynchronous_send_mail
=============================

A very simple wrapper around Django's built in send_mail to send email asynchronously using Python's threading - really useful for servers with slow internet connection. If you want more advanced features like mail queuing or scheduling you should look at other alternatives such as `Django Mailer <http://github.com/jtauber/django-mailer/>`_

OVERVIEW
========

For a more thorough explanation of what this bit of code tries to solve please visit:
http://ui.co.id/blog/asynchronous-send_mail-in-django

This is not intended to replace 

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
