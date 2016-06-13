# infrastructure-playpen
Deploy Apache Infrastructure VMs onto Vagrant

## background

Testing deployment changes to Apache infrastructure is too hard.  Specifically [infrastructure-puppet-kitchen](https://github.com/apache/infrastructure-puppet-kitchen) has too steep of a learning curve, and figuring out how to disable features that don't make sense on a throwaway VM is difficult.

Mid-to-long-term plans are to set up an Apache infrastructure playground making it easier to test out changes, but this is still a ways off.

Meanwhile, this [spike](http://agiledictionary.com/209/spike/) is an attempt to explore a simpler alternative using vagrant directly (i.e., without kitchen), with additions and removals of modules done via a YAML file.  For the moment, only whimsy-vm3 is supported, but adding others should be straightforward.

## installation instructions

1. Install and configure [infrastructure-puppet](https://github.com/apache/infrastructure-puppet), including installing `bundler` and running `bin/pull`.

2. Clone this repository

3. Run `infrastructure-playpen/provision`.

## plans

1. add more vms, and refactor as we go with the aim of reducing the overhead of supporting a new vm to be as small as possible.

2. explore having ASF infrastructure host a preconfigured common + ubuntu/1404 + colo/vagrant starter image to make testing go quicker.  Such an image would only need to be reasonably up to date as puppet will take care of the rest.
