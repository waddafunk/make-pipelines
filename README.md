# Shared CI Pipelines

A collection of reusable CI/CD pipelines, supporting both GitHub Actions and Woodpecker CI. These pipelines work in conjunction with standardized `make` targets to provide consistent development and testing workflows across projects, abstracting steps implementation. The idea is providing a consistent reusable structure for CI/CD shared among projects, defining abstract steps which concrete implementation is made in repo-specific makefiles. 

Implementations are provided for Github Actions ([Repo implementing this can be found here](https://github.com/waddafunk/CentralizedRateLimiter)) and for Woodpecker CI ([Find here an implementation I made to privately host your MLOps infrastructure on a raspberry PI, including woodpecker for CI/CD](https://github.com/waddafunk/tiny_mlops))

## Features

- 🎯 **Standardized CI/CD**: Consistent CI/CD automations throughout all your projects
- 🔧 **Make-Based step abstraction**: Just implement steps inside your makefile and have your CI/CD architecture ready
- 🔀 **CI Platform Agnostic**: Same workflow on both GitHub Actions and Woodpecker CI

## Prerequisites

- `make` installed on your system
- Access to either GitHub Actions or Woodpecker CI

## Usage

### 1. Set Up Make Targets

Ensure your project includes these standard make targets:

```makefile
dev-install  # Install development dependencies
format       # Run code formatters 
upgrade      # Upgrade syntax 
lint         # Run linters 
test         # Run test suite
```

## License

This project is licensed under the Apache 2.0 License - see the LICENSE file for details.