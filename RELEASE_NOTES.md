# STRATO Getting Started release notes

## 3.1.0

STRATO versions supported: v6.0.2+

- Removed OAUTH_ENABLED environment variable as obsolete (always true, non-OAuth mode is deprecated)
- Removed legacy support for STRATO versions 5 and older

## 3.0.4

STRATO versions supported: v4.0+

- Fixed the password not being set on slower machines due to race condition on node initial start
- Minor optimization fix for strato generation router script

## 3.0.3

STRATO versions supported: v4.0+

- Added --get-pubkey flag to obtain the node's public key

## 3.0.2

STRATO versions supported: v4.0+

- Remove blocdata docker volume on --drop-chains

## 3.0.1

STRATO versions supported: v4.0+

- Fix for backward compatibility for STRATO prior to version 5.5

## 3.0.0

STRATO versions supported: v4.0+

- Added support for STRATO 6.0
- Added router file to keep backward compatibility with STRATO 4 and 5

## 2.18.0

STRATO versions supported: v4.0+

- Remove docker volumes whether or not the down command was successful (for cases when docker network can't be removed etc.)

## 2.17.0

STRATO versions supported: v4.0+

- Fix for --fetch-logs not working correctly on some linux distributions

## 2.16.0

STRATO versions supported: v4.0+

- Fix for single node upgrade flow

## 2.15.0

STRATO versions supported: v4.0+

- scriptgen compatible with STRATO versions below 5.2.0
- updated formatting of scripts generated with scriptgen

## 2.14.0

STRATO versions supported: v4.0+

- scriptgen to add blockstanbul public key into generated run.sh scripts

## 2.13.0

STRATO versions supported: v4.0+

- scriptgen to add blockstanbulAdmins variable into generated run.sh scripts

## 2.12.0

STRATO versions supported: v4.0+

- OAUTH_SCOPE added to --help output

## 2.11.0

STRATO versions supported: v4.0+

- Added support for "port" in node-list.json syntax to alter the default STRATO port

## 2.10.1

STRATO versions supported: v4.0+

- Fail verbosely when no password can be read

## 2.10.0

STRATO versions supported: v4.0+

- Global in-memory password setting for STRATO 4.5+ with OAuth enabled

## 2.9.1

STRATO versions supported: v4.0+

- --drop-chains behavior fixed to remove the zookeeper volume

## 2.9.0

STRATO versions supported: v4.0+

- Support for STRATO container upgrade: --upgrade-strato --down and --drop-chains flags added, --remove flag deprecated

## 2.8.3

STRATO versions supported: v4.0+

- License agreement link changed in README.md

## 2.8.3

STRATO versions supported: v4.0+

- fixed issue with temporary directory creation and too verbose output in fetchlogs script

## 2.8.2

STRATO versions supported: v4.0+

- Automatically remove transient containers used for key generation

## 2.8.1

STRATO versions supported: v4.0+

- fetchlogs `--as-dir` flag added to output logs as directory and to not archive

## 2.8.0

STRATO versions supported: v4.0+

- fetchlogs python script added to fetch STRATO node logs and database dump (optional)
- `--fetch-logs` and `--fetch-logs-with-db` wrapper entrypoints to fetch logs easily
- minor refactoring


## 2.7.3

STRATO versions supported: v4.0+

- Fix for wrong "Node failed to start" message when running STRATO 4.3 or earlier

## 2.7.2

STRATO versions supported: v4.0+

- Suppress the unused variable warning messages in docker-compose

## 2.7.1

STRATO versions supported: v4.0+

- Wait for STRATO containers to become healthy
- -v|--version flag added
- BasicAuth is now off by default
- Minor refactoring

## 2.7

STRATO versions supported: v4.0+

- STRATO v4.3 compatibility
- Added the check of minimum required strato-getting-started version for docker-compose.yml provided
- Added OAuth help topic
- Some refactoring

## 2.6.1

- export blockstabul variable hotfix

## 2.6.0

- `--single` now runs a solo PBFT-blockstanbul node
- `--lazy` is added to run a single lazy mining PoW node (former --single)
- `--blockstanbul|-pbft` is added to run PBFT-blockstanbul node (equal to blockstanbul=true variable)
- `--stop` now only stops containers (can be started again)
- `--start` is added to start the stopped containers
- `--remove` is added to stop and remove containers, keep volumes (former --stop)
- Simple PBFT-blockstanbul variables checks added
- `--scriptgen` now generates scripts with --blockstanbul flag instead blockstanbul=true variable
- Some refactoring
