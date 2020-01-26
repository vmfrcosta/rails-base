source 'https://rubygems.org'
git_source(:github) { |repo| "https://github.com/#{repo}.git" }

ruby '2.6.5'

gem 'rack', '2.0.8' # Rack 2.1 is causing problems with Sidekiq. Remove this after it's fixed

# Rails Base
gem 'rails', '~> 6.0.0'
gem 'pg', '~> 1.0'
gem 'puma', '~> 4.3'
gem 'sass-rails', '~> 6'
gem 'webpacker', '>= 4.0'
gem 'turbolinks', '~> 5'
gem 'jbuilder', '~> 2.5'
gem 'bcrypt', '~> 3.1.7'
gem 'bootsnap', '>= 1.4.2', require: false
gem 'sprockets', '3.7.2', require: false

# Rails Session Store
gem 'redis', '~> 4.0'
gem 'hiredis'

# Rails Active Job
gem 'sidekiq'

# Rails Active Storage
gem 'image_processing', '~> 1.2'
gem 'aws-sdk-s3'

# User Agents
gem 'useragent'

# Email
gem 'postmark-rails'

# OAuth
gem 'omniauth', '~> 1.8'
gem 'omniauth-facebook', '~> 5.0'
gem 'omniauth-google-oauth2', '~> 0.5'

# PDF Generation
gem "wicked_pdf"
gem "prawn"
gem "combine_pdf"

# Website and Invitation image generation
gem 'selenium-webdriver'
gem 'webdrivers', '~> 4.0'

# Third Party Service: Payments
gem "pagarme"
gem "paypal-checkout-sdk", "~> 1.0.2"

# CSS
gem "autoprefixer-rails"

# Performance
#gem 'rack-mini-profiler'
#gem 'flamegraph'
#gem 'stackprof'

group :development, :test do
  gem 'byebug', platforms: [:mri, :mingw, :x64_mingw]
end

group :development do
  gem 'listen', '>= 3.0.5', '< 3.2'
  gem 'web-console', '>= 3.3.0'

  # PDF
  gem 'wkhtmltopdf-binary-edge'

  # Emails
  gem "letter_opener"

  # Linting
  gem 'rubocop', require: false
  gem 'rubocop-performance'
  gem 'rubocop-rails'
end

group :test do
  gem 'capybara', '>= 2.15', '< 4.0'

  # Heroki CI Parallel Testing
  gem 'knapsack_pro'

  # Handle Flakky Tests

end

group :production, :test do
  # Heroku PDF
  gem 'wkhtmltopdf-heroku'
end

group :production do
  # Exception Tracking
  gem 'sentry-raven'

  # Scaling
  gem 'rails_autoscale_agent'

  # Performance
  gem 'scout_apm'
end