# 2WT PHP 2023 - 2024: persoonlijk project

## Configure Homestead
- Update the file **C:\vagrant\homestead\Homestead.yaml**
  - Add the following code to the **sites** section:
    ```yaml
    sites:
        - map: project.test                        
          to: /home/vagrant/code/project/public
          php: "8.1"
        ...
    ```
  - Add a new **project** database to the **databases** section:
    ```yaml
    databases:
        - homestead
        - vinylshop
        - project
    ```
- Restart the virtual machine with option `2` in **laravel.bat**

## Clone this repository
- Clone this repository from the **Classroom link** to the folder **C:\Sites_laravel**
- Rename the folder to **project**
- Open the folder **C:\Sites_laravel\project** in PHPStorm
  - Rename the file **.env.project** to **.env**
  - Run the command `composer install` in the terminal
  - Run the command `npm install`
  - Configure PhpStorm (https://itf-laravel-10.netlify.app/config/laravel#configure-phpstormLinks)
  - Run the command `php artisan key:generate`
  - Run the command `php artisan storage:link`
  - Run the command `php artisan migrate` or `php artisan migrate:fresh`
  - Run the command `npm run watch` to open the project in the browser

## Tips
- Laravel 10 cheat sheet summary: (https://itf-laravel-10.netlify.app/config/cheatsheet)[https://itf-laravel-10.netlify.app/config/cheatsheet]
- Livewire 3 cheat sheet summary: (https://itf-laravel-10.netlify.app/config/cheatsheetLivewire)[https://itf-laravel-10.netlify.app/config/cheatsheetLivewire]
