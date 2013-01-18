# BytesConverter

Gem converting Kilobytes, Megabytes and Gigabytes into bytes.

## Installation

Add this line to your application's Gemfile:

    gem 'bytes_converter'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install bytes_converter

## Usage

first:

```require 'bytes_converter'```

Converting strings to bytes:

```BytesConverter::convert "some string"```

where "some string" can be anything like in these examples:

```BytesConverter::convert "12.3M" # --> 12897484.8
BytesConverter::convert "12.3" # --> 12.3 (no unit means bytes)
BytesConverter::convert "12.3 kilo bytes" # --> 12595.2
BytesConverter::convert "12.3 Megabytes" # --> 12897484.8
BytesConverter::convert "12.3 m" # --> 12897484.8
BytesConverter::convert "12.3 k" # --> 12595.2
BytesConverter::convert "12.3 bk" # --> 0.0 (b is not recognized)
BytesConverter::convert "12,3m" # --> 12897484.8
BytesConverter::convert "123" # --> 123
```

You can add new unit as a hash. Let's say you want OrangeBytes unit:

```orange = {"o" => 2}
BytesConverter::add_unit orange```

... and remove it with:

```BytesConverter::remove_unit "o"```

To get all available units:

```BytesConverter::get_units"```

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
