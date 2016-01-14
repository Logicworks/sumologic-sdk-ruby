Sumo Logic Ruby SDK
===================

[![Gem Version](https://badge.fury.io/rb/sumologic.svg)](http://badge.fury.io/rb/sumologic)
[![Build Status](https://img.shields.io/travis/grokify/sumologic-sdk-ruby/master.svg)](https://travis-ci.org/grokify/sumologic-sdk-ruby)
[![Code Climate](https://codeclimate.com/github/grokify/sumologic-sdk-ruby/badges/gpa.svg)](https://codeclimate.com/github/grokify/sumologic-sdk-ruby)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/grokify/sumologic-sdk-ruby/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/grokify/sumologic-sdk-ruby/?branch=master)
[![Docs](https://img.shields.io/badge/docs-rubydoc-blue.svg)](http://www.rubydoc.info/gems/sumologic/)
[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/grokify/sumologic-sdk-ruby/master/LICENSE.txt)

Ruby interface to the Sumo Logic REST API.

## Usage

The interface for this SDK is still being built out to follow the structure in the 
[Sumo Logic Python SDK](https://github.com/SumoLogic/sumologic-python-sdk).

The following methods are currently implemented:

```ruby
sumo = SumoLogic::Client.new(access_id, access_key)

# Search
r = sumo.search(query [, from, to, time_zone])

r = sumo.search_job(query [, from, to, time_zone])

r = sumo.search_job_records({'id' => search_job_id}, limit, offset)

r = sumo.search_job_status( {'id' => search_job_id})

# Dashboards
r = sumo.dashboards()

r = sumo.dashboard(dashboard_id)

r = sumo.dashboard_data(dashboard_id)
```

Note, for the search methods, the query parameter can be exactly the same query that is entered into the Sumo Logic web console.

Example scripts are located in the `scripts` directory of the [GitHub repo](https://github.com/grokify/sumologic-sdk-ruby).

## Change Log

See [CHANGELOG.md](CHANGELOG.md).

## Links

Project Repo

* https://github.com/grokify/sumologic-sdk-ruby

Sumo Logic API Documentation

* https://github.com/SumoLogic/sumo-api-doc/wiki

Sumo Logic Python SDK

* https://github.com/SumoLogic/sumologic-python-sdk

## Contributions

Please add your scripts and programs to the `scripts` folder.

Any reports of problems, comments or suggestions are most welcome.

Please report these on [Github](https://github.com/grokify/sumologic-sdk-ruby)

## License

Sumo Logic Ruby SDK is available under an MIT-style license. See [LICENSE.txt](LICENSE.txt) for details.

Sumo Logic Ruby SDK &copy; 2015-2016 by John Wang
