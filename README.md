# Homebrew tap for MyMicroTunnel

MyMicroTunnel publishes a port on your machine at a hostname you own, over a
WireGuard tunnel to a gateway in your own AWS account.

```sh
brew tap IceSkatingCoach/mymicrotunnel
brew install --cask mymicrotunnel
```

The cask installs the signed, notarized package from
<https://downloads.maragato.ca>, which is the same build the app updates
itself from. Source, licence and documentation live in
[IceSkatingCoach/MyMicroTunnel](https://github.com/IceSkatingCoach/MyMicroTunnel).

## Uninstalling

Remove the AWS side first, while the profiles are still on the machine:

```sh
mymicrotunnel uninstall
brew uninstall --cask mymicrotunnel
```

`brew uninstall` on its own leaves the deployed stack running, and running
costs money. Add `--zap` to also remove the profile store and the tunnel
configuration under `/etc/wireguard`.

## This file is generated

`Casks/mymicrotunnel.rb` is written by `make cask` in the main repository, so
the version and the checksum always describe a release that was actually
built and published. Fix the generator there rather than editing the cask
here.
