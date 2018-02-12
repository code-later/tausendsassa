# Tausendsassa

Tausendsassa is minimal web framework in the spirit of Sinatra written in [Halunke](http://halunke.jetzt/).

A very simple app would look like:

```hal
('HelloWorld = [
  ["GET /hello/:world" { |'params 'env|
    [
      200
      @["ContentType" "text/plain"]
      [
        ("Hello " + (params @ "world" else ""))
        "\n"
        ("Say what? " + (params @ "say" else "Nothing to say!"))
      ]
    ]
  }]
])

(web run (Tausendsassa with HelloWorld) on "0.0.0.0:3000")
```

## License

The project is available as open source under the terms of the [MIT
License](https://opensource.org/licenses/MIT).

## Code of Conduct

Everyone interacting in the Halunke project’s codebases, issue trackers, chat
rooms and mailing lists is expected to follow the [code of
conduct](https://github.com/moonglum/halunke/blob/master/CODE_OF_CONDUCT.md).
