## [Laravel](http://laravel.com/) for [Google App Engine](https://cloud.google.com/appengine/)
This repository contains a modified Laravel Starter app for Google App Engine.

## Installation

1. Clone the repository with

        git clone https://github.com/GoogleCloudPlatform/laravel.git

1. Follow the [PHP Tutorial](https://cloud.google.com/appengine/docs/php/gettingstarted/introduction) if you have never used App Engine before.

1. Create a CloudSQL instance based on [these instructions](https://cloud.google.com/appengine/docs/php/cloud-sql/#create). Also [create a database](https://cloud.google.com/sql/docs/create-database) for storing the [Eloquent ORM](http://laravel.com/docs/5.0/eloquent).

1. Replace `<project-id>`, `<instance-id>` and `<database-name>` in [app.yaml](app.yaml) with the corresponding value for your Google Cloud project and ClouSQL instance. By default, the app will store the cache files and logs at a specific location in the app's default GCS bucket. This can be changed by altering the `STORAGE_PATH` environmental variable in [app.yaml](app.yaml). Remember to also update `google_app_engine.allow_include_gs_buckets` to match the new value in [php.ini](php.ini).

1. Install [composer](https://getcomposer.org/) if you haven't done so previously. To install all required dependencies, run the following command from your project's root, which is the directory that contains [composer.json](composer.json).

        php composer.phar install

1. [Deploy your app](https://cloud.google.com/appengine/docs/php/gettingstarted/uploading).

1. Access your app using http://your_project_id.appspot.com/ and you should see Laravel's default welcome page.

## Troubleshooting

1. If Composer fails to download the dependencies, make sure that your local PHP installation satisfies Composer's [system requirements](https://getcomposer.org/doc/00-intro.md#system-requirements). Specifically, [cURL](http://php.net/manual/en/book.curl.php) support is required.

1. If you see errors about missing the default Cloud Storage bucket, follow the [cloud integration instructions](https://cloud.google.com/appengine/docs/php/googlestorage/setup) to create a default bucket for your project.

## Contributing
Have a patch that will benefit this project? Awesome! Follow these steps to have it accepted.

1. Please sign our [Contributor License Agreement](CONTRIB.md).
1. Fork this Git repository and make your changes.
1. Create a Pull Request
1. Incorporate review feedback to your changes.
1. Accepted!

## License
All files in this repository are under the [MIT License](LICENSE) unless noted otherwise.
