# Phauxth

[![Hex.pm Version](http://img.shields.io/hexpm/v/phauxth.svg)](https://hex.pm/packages/phauxth)
[![Join the chat at https://gitter.im/phauxth_elixir/Lobby](https://badges.gitter.im/phauxth_elixir/Lobby.svg)](https://gitter.im/phauxth_elixir/Lobby?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Authentication library for Phoenix web apps.

## Getting started with Phauxth and Phoenix

### Create new Phoenix project

Run the following commands (replace alibaba with the name of your project):

    mix phx.new alibaba
    cd alibaba

To create an api, change the `mix phx.new` command to:

    mix phx.new alibaba --no-html --no-brunch

### Run the Phauxth installer

N.B. if you are not using Erlang 20, you might have to build the installer
yourself. You can find the instructions in the README in the installer/new
directory.

Download and install the [phauxth_new installer](https://github.com/riverrun/phauxth/raw/master/installer/archives/phauxth_new.ez).

    mix archive.install https://github.com/riverrun/phauxth/raw/master/installer/archives/phauxth_new.ez

For a basic setup, run the following command:

    mix phauxth.new

If you want to add email / phone confirmation and password resetting, add the `--confirm` option:

    mix phauxth.new --confirm

If you want to create authentication files for an api, use the `--api` option:

    mix phauxth.new --api

### Add phauxth to deps

1. Make sure you are using Elixir 1.4 or above.

2. Add phauxth to your `mix.exs` dependencies

    ```elixir
    defp deps do
      [{:phauxth, "~> 0.12-rc"}]
    end
    ```

3. Run `mix deps.get`

4. Add the `get(id)` and `get_by(attrs)` functions to your user Accounts module

See the [wiki](https://github.com/riverrun/phauxth/wiki) for more
information about Phauxth.

### License

BSD
