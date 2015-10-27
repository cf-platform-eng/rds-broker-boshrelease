# AWS RDS Service Broker BOSH Release

This is a [BOSH](http://bosh.io/) release for the [AWS RDS Service Broker](https://github.com/cf-platform-eng/rds-broker).

## Disclaimer

This is NOT presently a production ready [AWS RDS Service Broker](https://github.com/cf-platform-eng/rds-broker) BOSH release. This is a work in progress. It is suitable for experimentation and may not become supported in the future.

## Usage

### Using BOSH

#### Upload the BOSH release

To use this BOSH release, first upload it to your BOSH:

```
bosh target BOSH_HOST
git clone https://github.com/cf-platform-eng/rds-broker-boshrelease.git
cd rds-broker-boshrelease
bosh upload release releases/rds-broker/rds-broker-2.yml
```

#### Create a BOSH deployment manifest

Now create a deployment file (using the files at the [examples](https://github.com/cf-platform-eng/rds-broker-boshrelease/blob/master/examples/) directory as a starting point).

#### Deploy using the BOSH deployment manifest

Using the previous created deployment manifest, now we can deploy it:

```
bosh deployment path/to/deployment.yml
bosh -n deploy
```

Refer to the [AWS RDS Service Broker Documentation](https://github.com/cf-platform-eng/rds-broker/blob/master/CONFIGURATION.md) for more details about the required properties.

### Using [Pivotal Ops Manager](https://network.pivotal.io/products/ops-manager)

### Build the Pivotal tile

First you will need to build the Pivotal tile:

```
git clone https://github.com/cf-platform-eng/rds-broker-boshrelease.git
cd rds-broker-boshrelease
bundle exec vara build-pivotal .
```

### Upload the Pivotal tile

Upload the Pivotal tile `p-rds-broker-0.1.0.0.pivotal` to your Pivotal Ops Manager, configure it, and deploy.

## Contributing

In the spirit of [free software](http://www.fsf.org/licensing/essays/free-sw.html), **everyone** is encouraged to help improve this project.

Here are some ways *you* can contribute:

* by using alpha, beta, and prerelease versions
* by reporting bugs
* by suggesting new features
* by writing or editing documentation
* by writing specifications
* by writing code (**no patch is too small**: fix typos, add comments, clean up inconsistent whitespace)
* by refactoring code
* by closing [issues](https://github.com/cf-platform-eng/rds-broker-boshrelease/issues)
* by reviewing patches

### Submitting an Issue
We use the [GitHub issue tracker](https://github.com/cf-platform-eng/rds-broker-boshrelease/issues) to track bugs and features. Before submitting a bug report or feature request, check to make sure it hasn't already been submitted. You can indicate support for an existing issue by voting it up. When submitting a bug report, please include a
[Gist](http://gist.github.com/) that includes a stack trace and any details that may be necessary to reproduce the bug,. Ideally, a bug report should include a pull request with failing specs.

### Submitting a Pull Request

1. Fork the project.
2. Create a topic branch.
3. Implement your feature or bug fix.
4. Commit and push your changes.
5. Submit a pull request.

## Copyright

Copyright (c) 2015 Pivotal Software, Inc. See [LICENSE](https://github.com/cf-platform-eng/rds-broker-boshrelease/blob/master/LICENSE) for details.
