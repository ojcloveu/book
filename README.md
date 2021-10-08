##### Deployment

1.  Extract the archive and put it in the folder you want
2.  Run `cp .env.example .env` file to copy example file to `.env`  
    Then edit your `.env` file with DB credentials and other settings.
3.  Run `composer install` command
4.  Run `php artisan migrate --seed` command.  
    Notice: seed is important, because it will create the first admin user for you.
5.  Run `php artisan key:generate` command.
6.  Run `npm install`
7.  Run `npm run dev`
8.  If you have file/photo fields, run `php artisan storage:link` command.
9.  Laravel Sanctum for API Auth: If you are using custom hostname for project other than localhost make sure that value of `SANCTUM_STATEFUL_DOMAINS` variable in `.env` file is the same as your hostname in browser. Example: `SANCTUM_STATEFUL_DOMAINS=myproject.test`

And that's it, go to your domain and login:

##### Default credentials

Username: `admin@admin.com`  
Password: `password`

For more information, potential errors and related links, you can read [more detailed installation guide here](https://helpdocs.quickadminpanel.com/using-generated-code/download-code-and-install-your-web-server)
