# Docker

The Docker configuration for Cal is an effort powered by people within the community. Cal does not provide official support for Docker, but we will accept fixes and documentation. Use at your own risk.

The Docker configuration can be found [in our docker repository](https://github.com/calendso/docker).

## Requirements
Make sure you have `docker` & `docker-compose` installed on the server / system.

## Getting Started

1. Clone calendso-docker

    ```bash
    git clone git@github.com:calendso/calendso-docker.git --recursive
    ```

2. Update `.env` if needed

3. Build and start calendso

    ```
    docker-compose up --build
    ```

4. Start prisma studio
    ```
    docker-compose exec calendso -- npx prisma studio
    ```
5. Open a browser to [http://localhost:5555](http://localhost:5555) to look at or modify the database content.

6. Click on the `User` model to add a new user record.
7.  Fill out the fields (remembering to encrypt your password with [BCrypt](https://bcrypt-generator.com/)) and click `Save 1 Record` to create your first user.
8. Open a browser to [http://localhost:3000](http://localhost:3000) and login with your just created, first user.