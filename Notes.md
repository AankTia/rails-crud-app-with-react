# Learn & Parctice CRUD with Rails & React.js

## Source :

### Let's build a CRUD app with Ruby on Rails and React.js

- **[Part-1](https://youtu.be/oyjzi837wME?si=5mG2ldgOrUJub4t1)**
- **[Part-2]()**
- **[Part-3]()**
- **[Part-4]()**

## Development Step-by-step

1. Create new Rails project with PostgreSQL
   `rails new rails-crud-app-with-react --database=postgresql --javascript=esbuild --css=sass`

2. Install dependencies
   `bundle install`

3. Setup React and other JavaScript dependencies

```
cat << 'EOF' > package.json
{
  "name": "app",
  "private": "true",
  "dependencies": {
    "@hotwired/stimulus": "^3.2.1",
    "@hotwired/turbo-rails": "^7.3.0",
    "@popperjs/core": "^2.11.8",
    "axios": "^1.4.0",
    "bootstrap": "^5.3.0",
    "esbuild": "^0.18.11",
    "react": "^18.2.0",
    "react-dom": "^18.2.0",
    "react-router-dom": "^6.14.1",
    "sass": "^1.63.6"
  },
  "scripts": {
    "build": "esbuild app/javascript/*.* --bundle --sourcemap --outdir=app/assets/builds --public-path=/assets",
    "build:css": "sass ./app/assets/stylesheets/application.sass.scss:./app/assets/builds/application.css --no-source-map --load-path=node_modules"
  }
}
EOF
```

4. Install npm packages
   `yarn install`

5. Setup database configuration
   `bundle exec rails db:create`
