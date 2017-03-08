# Localtower

### See the schema
![Schema](https://raw.githubusercontent.com/damln/localtower/master/public/1_schema.png)

### Create a model
![Models](https://raw.githubusercontent.com/damln/localtower/master/public/2_models_1.png)

### Create a many to many relation
![Relations](https://raw.githubusercontent.com/damln/localtower/master/public/3_relations.png)

### Create a migration
![Migrations](https://raw.githubusercontent.com/damln/localtower/master/public/4_migrations.png)


## INSTALL

Add to your Gemfile:

    # In your Gemfile

    group :development do
      gem "localtower"
    end

In your terminal:

    bundle install

Add to your routes:

    # in config/routes.rb

    if Rails.env.development?
      mount Localtower::Engine, at: "localtower"
    end

## USAGE

Open your browser at: `http://localhost:3000/localtower`

## TEST

Create a .env file inside the spec/dummy folder with the credentials to your PostgreSQL Database. It should look like this:

spec/dummy/.env:

    LOCALTOWER_PG_USERNAME="admin"
    LOCALTOWER_PG_PASSWORD="root_or_smething"

Run the spec:

    bundle install
    bundle exec rspec spec/

Notes:
Tests are currently very slow because this is testing rails commands so it boots the rails for each test. Zeus or spring should be introced.
