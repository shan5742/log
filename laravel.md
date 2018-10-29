# Laravel

I'm now beginning to look at the **Laravel** PHP framework, I recently got everything installed on my local machine following a mix of the following two links:

- [code-mentor](https://www.codementor.io/saquibgt/how-to-create-lamp-stack-with-laravel-on-ubuntu-server-b7gt8cpy1)
- [how-to-forge](https://www.howtoforge.com/tutorial/install-laravel-on-ubuntu-for-apache/)

I will write a brief overview below to act as notes for myself in case I need to refer back to.

1. update system
2. install Apache
3. edit `000-default.conf` from `html` to `public_html`
4. restart apache server
5. install MYSQL
6. run `mysql_secure_installation`
7. install PHP
8. install Composer
9. install Laravel project via composer in the `/var/www/public_html` directory
10. Done!

That is the basic overview of the setup. From here I plan to build out various Laravel projects.
