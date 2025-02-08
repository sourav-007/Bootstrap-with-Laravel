# Bootstrap with Laravel Jetstream

This guide will help you configure **Bootstrap** with **Laravel Jetstream** in your Laravel project.


## Step 1: Install Laravel Jetstream  

First, ensure you have Laravel installed. Then, install Jetstream with **Livewire**:  

### Installing Jetstream ​

```
composer require laravel/jetstream
```


### Install Jetstream With Livewire

```
Install Jetstream With Livewire ​
```

If you would like **teams** support, you can provide the `**--teams**` directive to the install command:

```
php artisan jetstream:install livewire --teams
```

Or, Install Jetstream With Inertia

```
php artisan jetstream:install inertia
```

If you would like **teams** support with the Inertia stack, provide the `**--teams**` directive to the install command:

```
php artisan jetstream:install inertia --teams
```

The Inertia stack may also be installed with SSR support:

```
php artisan jetstream:install inertia --ssr
```

**Dark Mode** <br>
<span style="font-weight:100; font-size:13px;">
    If you would like to include "dark mode" support when scaffolding your application's frontend, provide the --dark directive when executing the jetstream:install command:
</span>
<br>

```
php artisan jetstream:install livewire --dark
```

Finalizing the Installation ​<br>
<span style="font-weight:100; font-size:13px;">
    After installing Jetstream, you should install and build your NPM dependencies and migrate your database:
</span>
<br>

```
npm install
npm run build
php artisan migrate
```


## Step 2: Remove Tailwind CSS

Remove Tailwind CSS from your project, as it's the default:

```
npm uninstall tailwindcss postcss autoprefixer
```
Then, remove any Tailwind imports from your CSS files, typically found in resources/css/app.css.



## Step 3: Install Bootstrap

Install Bootstrap via npm:

```
npm install bootstrap
```

## Step 4: Include Bootstrap in Your Project

Import Bootstrap into your project. You can do this by adding the following line to your resources/css/app.css or create a new SCSS file if you prefer using SCSS:

```
@import 'bootstrap/dist/css/bootstrap.min.css';
```

Alternatively, for SCSS:

```
@import '~bootstrap/scss/bootstrap';
```

Then, update your `webpack.mix.`js to compile the new CSS:

```
const mix = require('laravel-mix');

mix.js('resources/js/app.js', 'public/js')
    .postCss('resources/css/app.css', 'public/css', [
        //
    ]);
```

## Step 5: Adjust Your Views

You will need to update your Blade templates to use Bootstrap classes instead of Tailwind. This involves changing class names in the HTML structure of your Jetstream views, which can be found in `resources/views`.

## Step 6: Compile Assets

Run the following command to compile your assets:

```
npm run dev
```

## Step 7: Test Your Application

Make sure to test your application thoroughly to ensure that all styles and scripts are loading correctly and that the UI looks as expected.


## Conclusion

By following this guide, you have successfully replaced **Tailwind CSS** with **Bootstrap** in your Laravel Jetstream project. Now, your application is fully configured with Bootstrap's styling framework while still benefiting from Jetstream's powerful authentication and user management features.



## 🔗 Links
[![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/souravsaha21/)

