# elixir-docker-template

this repository is built for people who just want to have the elixir as a process container and use all the functions without installing anything but docker to the host machine environment. The docker containers of this image are already connected to the host folder, so any script you write can run without rebuilding the image or anything.

## Setup 

Clone this repo, install docker, run this on the bash of the host enviroment that docker is running

### `docker-compose up`

# Important Notice

This image also has a built in bash on top of the elixir-alpine. This helps us to have the ability of going through our files inside the container and run any script easily inside the elixir environment while also benefitting from the lightweight release of the elixir-alpine. 

Full release is 1 GB and this way, we only run the environment with a setup of 90 MBs by only having the things we really need to be able to run exs files. We can also add more stuff whenever needed.



## Good To Know

### `docker-compose up`

Run this whenever you want an elixir environment.

### `docker exec -it ead_elixir_number-of-container bash`

Run this on another bash tab for any number of the elixir container to acces it's bash. They have the host folder binded and run as a service, so whatever you update in the main folder of the container on host will be updated also on the container.

### `elixir your-script-name.exs`

Once in bash of the container, you can easily run the exs files by going into the folder where the exs file is and just run the command above with your exs file being the argument for the elixir command.

### `docker exec -it ead_elixir_number-of-container iex`

Use this to run an iex session on a specific elixir container.

### `docker-compose up --build`

Run this whenever you want to rebuild the image.

### `docker run -it --rm ead_elixir bash`

Use this to open the bash of an elixir container that is not binded to the host folder.

### `docker run -it --rm ead_elixir`

Use this to run a new iex session.

## Contributing

1. Fork it (<https://github.com/murikarox/base-setup-drd.git/fork>)
2. Create your feature branch (`git checkout -b feature/something`)
3. Commit your changes (`git commit -am 'Added Something`)
4. Push to the branch (`git push origin feature/something`)
5. Create a new Pull Request

## Maintainers

Murat Eksi – info@murateksi.com

## License
[MIT](https://choosealicense.com/licenses/mit/)

