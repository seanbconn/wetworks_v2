# ENTR-451 Starter Template for Rails

This is a template used to built the real templates used in class... can always add or remove things as needed.

### Assumptions

- We don't need to send or receive mail
- We don't need WYSIWYG (Action Text)
- We don't need async jobs
- We don't need WebSockets (could change to add Hotwire later)
- We don't need an asset pipeline – use `script` tags for things like Bootstrap/Tailwind and the `public` directory for assets
- We don't need JavaScript 🤘
- We don't need Hotwire
- We don't need JBuilder
- We don't need tests
- We don't need Bootsnap

### Notes on generating this template

Started with a `rails new`, ignoring most features based on the assumptions above:

```
rails new . --skip-action-mailer --skip-action-mailbox --skip-action-text --skip-active-job --skip-action-cable --skip-asset-pipeline --skip-javascript --skip-hotwire --skip-jbuilder --skip-test --skip-system-test --skip-bootsnap
```

Then:

- Add a `.gitpod.yml` file, so that it runs `bundle install` upon initial opening of workspace
- Strips to bare-minimum `Gemfile` (Rails 7 default based on the above generator is already pretty good)
- Modify `development.rb` to allow development hosts and to remove helpers, asset pipeline, and test framework
- Modify `application.rb` to disable `belongs_to` validation and to disable strong parameters (yes, mass-assignment is bad but learning is hard)
- Add `public/stylesheets/application.css`
- ~~DO NOT ignore development.sqlite3~~ back to ignoring it... because template repos are created on top of template repos, this gets hairy

### Getting Started

1. Copy from template
2. Open copied repository in Gitpod (or IDE of choice)
3. Make any desired changes to `db/migrate/*_create_users.rb` migration file
4. Run `rails db:setup` to create database and add users table