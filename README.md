# jekyll-bootstrap-resume-theme

This is a resume theme based on [Start Bootstrap Resume](https://github.com/startbootstrap/startbootstrap-resume).

## Installation

Add this line to your Jekyll site's `Gemfile`:

```ruby
gem "jekyll-bootstrap-resume-theme"
```

And add this line to your Jekyll site's `_config.yml`:

```yaml
theme: jekyll-bootstrap-resume-theme
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install jekyll-bootstrap-resume-theme

## Usage

### Change Basic information
in `_config.yml` you can change basic information such as your website name and description.

### Change Profile Picture
Change your profile picture (the one that is visible on the side menu) by replacing the image present in `assets/img/profile.jpg` with your own picture. Make sure it is in `jpg` format and has the name `profile`.

### Changing Profile information
Change your name, email, address, phonenumber, by going to `_config.yml` and giving new values to each item under `portfolio.info`.

This should look something like:
```yaml
portfolio:
  info:
    name:
      firstname: John
      lastname: Doe
    location: 3542 Berry Street · Cheyenne Wells, CO 80810
    phonenumber: (317) 585-8468
    email: name@email.com
```

### Changing Social Media
At the moment 5 icons are supported: LinkedIn, Github, Facebook, Twitter and Custom Site.

These can be enabled/disabled and links can be changed by uncommenting and changing the text in `_config.yml` under `portfolio.social`.
So let's say you want to only have linkedIn and github enabled then you'd have something like this:
```yaml
portfolio:
  social:
    # twitter: your-username
    # facebook: your-username
    github: your-username
    linkedin: your-username
    # rss: 'your-website'
```

Where `your-username` and `your-website` would be either your username or your website url.
If a `#` is present before the item, then the item is commented, and won't be displayed on the website.

### Changing About information
Change the introduction text in the `About` section by going to `index.md` and changing the text with whatever text you want to have.

Important: DO NOT REMOVE THE BELOW TEXT FROM THE `index.md` file.
```
---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: resume
---
```

### Experience, Education, Projects, etc...
Sections such as experience, education and projects are handled through so called `data files`.
These files can be found in the `_data` directory, and each section has its own file.

Below tables will be shown with each section and the possible fields.

#### Experience
File name: `_data/jobs.json`

| field name     | data type | format     | required  |
|----------------|-----------|------------|-----------|
| function       | text      | ""         | yes       |
| company        | text      | ""         | yes       |
| start_date     | date      | dd-mm-yyyy | yes       |
| end_date       | date      | dd-mm-yyyy | no        |
| description    | text      | ""         | no        |

#### Education
File name: `_data/studies.json`

| field name     | data type | format     | required  |
|----------------|-----------|------------|-----------|
| course         | text      | ""         | yes       |
| school         | text      | ""         | yes       |
| degree         | text      | ""         | no        |
| start_date     | date      | dd-mm-yyyy | yes       |
| end_date       | date      | dd-mm-yyyy | no        |
| description    | text      | ""         | no        |

#### Volunteering Work
File name: `_data/volunteers.json`

| field name     | data type | format     | required  |
|----------------|-----------|------------|-----------|
| function       | text      | ""         | yes       |
| company        | text      | ""         | yes       |
| start_date     | date      | dd-mm-yyyy | yes       |
| end_date       | date      | dd-mm-yyyy | no        |
| description    | text      | ""         | no        |

#### Projects
File name: `_data/projects.json`

| field name          | data type | format     | required  |
|---------------------|-----------|------------|-----------|
| title               | text      | ""         | yes       |
| stakeholders        | text      | ""         | no        |
| start_date          | date      | dd-mm-yyyy | yes       |
| end_date            | date      | dd-mm-yyyy | no        |
| description         | text      | ""         | no        |

#### Awards
File name: `_data/awards.json`

Just an array of strings.

```
[
  "This is an Award",
  "This is another award"
]
```

#### Skills
File name: `_data/skills.json`

Just an array of strings.

```
[
  "Java",
  "C#",
  "VueJS"
]
```

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/[USERNAME]/hello. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## Development

To set up your environment to develop this theme, run `bundle install`.

Your theme is setup just like a normal Jekyll site! To test your theme, run `bundle exec jekyll serve` and open your browser at `http://localhost:4000`. This starts a Jekyll server using your theme. Add pages, documents, data, etc. like normal to test your theme's contents. As you make modifications to your theme and to your content, your site will regenerate and you should see the changes in the browser after a refresh, just like normal.

When your theme is released, only the files in `_layouts`, `_includes`, `_sass` and `assets` tracked with Git will be bundled.
To add a custom directory to your theme-gem, please edit the regexp in `jekyll-bootstrap-resume-theme.gemspec` accordingly.

## License

The theme is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).
