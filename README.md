# aws-scripts
Scripts that simplify AWS CLI usage.

## aws-codebuild

Script for starting codebuild passing only project name, source version and env variables (not required) as parameters.

### Installation

```
    curl https://raw.githubusercontent.com/IQ-tech/aws-scripts/master/aws-codebuild > /usr/local/bin/aws-codebuild
    chmod +x /usr/local/bin/aws-codebuild
```

### Usage

```
    aws-codebuild <project-name> <source-version> [<env-var>=<value> ...]
```

#### Example

```
    aws-codebuild messaging-services master ENVIRONMENT=development SERVICE=messages-process
```

### Usage with aws-okta

```
    aws-okta exec <profile>  -- aws-codebuild <project-name> <source-version> [<env-var>=<value> ...]
```

aws-okta: https://github.com/segmentio/aws-okta
