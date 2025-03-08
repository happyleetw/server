# Share Note backend server

Backend server for [Share Note](https://github.com/alangrainger/share-note/).

## Run with Docker

1. Take a copy of the [docker-compose.yml](https://github.com/note-sx/server/blob/main/docker-compose.yml) file
2. Take a copy of the [example env file](https://github.com/note-sx/server/blob/main/.env.example) and save as `.env`
3. Update the `.env` options as below
4. `docker-compose up -d`

## `.env` options

| Option                      | Example             | Description                                                                                                                              |
|-----------------------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| BASE_WEB_URL                | https://example.com | The base public URL for your server.                                                                                                     |
| HASH_SALT                   | Any random string   |                                                                                                                                          |
| MAXIMUM_UPLOAD_SIZE_MB      | 5                   | The maximum allowed size for user uploads in megabytes (MB).                                                                             |
| FOLDER_PREFIX               | 0                   | *OPTIONAL.* Set this to `1` or `2` if you want user files to be split into subfolders based on the first *N* characters of the filename. |
| CLOUDFLARE_TURNSTILE_KEY    |                     | *OPTIONAL.* If you want to use Turnstile to show a captcha when someone creates an account.                                              |
| CLOUDFLARE_TURNSTILE_SECRET |                     | *OPTIONAL.* If you want to use Turnstile to show a captcha when someone creates an account.                                              |
| CLOUDFLARE_ZONE_ID          |                     | *OPTIONAL.* If you want to use Cloudflare proxy in front of your server.                                                                 |
| CLOUDFLARE_API_KEY          |                     | *OPTIONAL.* If you want to use Cloudflare proxy in front of your server.                                                                 |
