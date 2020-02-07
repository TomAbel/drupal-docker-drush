# Drupal-Docker-Drush

Automatically set up a Drupal 8 install with Drush.
All in a Docker container, with credentials as root admin.
## Getting Started

```
docker-compose up -d
```

### Prerequisites

What things you need to install the software and how to install them

```
Docker Compose
https://docs.docker.com/compose/install/
```

### Installing

A step by step series of examples that tell you how to get a development env running

Git clone repository

```
git clone https://github.com/TomAbel/drupal-docker-drush
```
Change directory to it
```
cd drupal-docker-drush
```

Start up Docker

```
docker-compose up -d
```

Modules can be installed by adding this to docker-compose.yml

```
- ./mymodule:/var/www/html/modules/mymodule
```

and specifiying it in drush_install.sh

```
        --account-mail=testing@demo.sandbox \
        --account-name=root \
        --account-pass=admin
    drush en -y mymodule
```

## Built With

* [Docker](https://www.docker.com/) - Container
* [Drush](https://maven.apache.org/) - DRUpal SHell
* [Drupal](https://rometools.github.io/rome/) - Content management framework

## Contributing

Issues and pull requests are welcome.


## Acknowledgments

* Hat tip to Smaily
