# Changelog

All notable changes to the `python-domino` library will be documented in this file.

## [Unreleased]

### Added
* Added black and flake8 formatting
* Implemented pre-commit for black / flake8 formatting.
* Added / updated dataset endpoint usability.

### Changed
* updated airflow dependency 2.2.4
* Updated runs_stdout output

## 1.0.8

### Added

### Changed
* Updated authentication methods precedence.
* Changed version number message logging level to debug

## 1.0.7

### Added
* Added support for MPI cluster type in job_start
* Added support for overriding the default hardware tier by id when starting a job

### Changed
* Overriding the hardware tier by name has been marked as deprecated

## 1.0.6

### Added

* Automatically re-read auth token from file to avoid reusing short-lived access tokens
* Better token expiration error handling for job_start and runs_start methods
* Added support for external volume mounts in job_start

### Changed

## 1.0.5

### Added

* Added support for launching jobs with Dask clusters via job_start
* Added the ability to choose which exceptions to ignore (if any) while polling for `job_start_blocking`
* Added several new unit tests in `test_basic_auth.py` and `test_jobs.py`
* Added a public method to re-authenticate if a token expires (assuming a long-running process)
* Allow `auth_token` to be passed as a string to the `__init__()` method

### Changed

## 1.0.4

### Added

* `collaborators_remove` method
* Model export and AWS SageMaker API integration

### Changed

* Model version publish method (model_version_publish) doesn't take name anymore
* `collaborators_add` method changed to use v4 API

## 1.0.3

### Added

* Add v4 API endpoint `job_start` to start job with `onDemandSparkCluster` option
* Add v4 API endpoint `job_stop`, `job_status` & `job_start_blocking`

### Changed

* Started caching project_id
* Started using request session instead of creating new session every time
* Check if an App is running before attempting to stop it (in `app_unpublish`)

## 1.0.2

### Added

* Added HW tier validation in DominoOperator
* Added ENV Variable `DOMINO_LOG_LEVEL` to set log level

### Changed

* Fixed issue in `run_stop` method
* Better logging in `runs_start_blocking` method
* Added raise for error code (4xx & 5xx)
* Fixed library initialization error in case host url had trailing slash
* Fix app publish issue with domino 4.3

## 1.0.1

### Added

* HW tier functions.
* Airflow DominoOperator support.

### Changed

* Better error handling in `runs_start_blocking`.

## 1.0.0

### Added

* `Domino`/`python-domino` version compatibility matrix.
* Installation instructions for older `python-domino` version.
* `retry` parameter for `runs_start_blocking` method.
* Support for Domino authentication tokens.

### Changed

* Fixed issues in `model_version_publish` method.
* Fixed issues in `app_publish` and `app_unpublish` methods.
* Fixed issues in `project_create`, `fork_project` and `collaborators_add` methods.
