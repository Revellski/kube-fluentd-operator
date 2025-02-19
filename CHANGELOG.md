# CHANGELOG

## [v1.14.0](https://github.com/vmware/kube-fluentd-operator/releases/tag/v1.14.0)

#### Core:
  - Make fluentd log level configurable (#196) (@kkapoor1987)
  - feat(kubectl): add manifests for kubectl install (#192) (@Cryptophobia)
  - feat(fluentd): upgrade fluentd to v1.12.2 (#193) (@Cryptophobia)
  - feat(reloader): sorts configs so they are ordered (#194) (@Cryptophobia)
  - chore(base-image): upgrade gems and bundler (#195) (@Cryptophobia)
       - upgrade ruby to 2.7.3
       - upgrade bundler to 2.2.15
  - chore(go): upgrade to go1.16 and add linting (#197) (@Cryptophobia)

#### CI:
  - chore(go): upgrade to go1.16 and add linting (#197) (@Cryptophobia)

#### Helm:
  - Make fluentd log level configurable (#196) (@kkapoor1987)

## [v1.14.0-beta.3](https://github.com/vmware/kube-fluentd-operator/releases/tag/v1.14.0-beta.3)

#### Core:
  - Move to graceful reload endpoint and error (#189) (@slimm609)
  - fix(config-reloader): add timeout seconds on startup (#190) (@Cryptophobia)
  - chore(base-image): upgrade to use photon:4.0 (#186) (@Cryptophobia)

#### Plugins:
  - chore: upgrade vmware-log-intelligence to 2.0.6 (#187) (@Cryptophobia)

## [v1.14.0-beta.2](https://github.com/vmware/kube-fluentd-operator/releases/tag/v1.14.0-beta.2)

#### Core:
  - Migrate to go modules (#152) (@viveksyngh)
  - Add timeout and log for validation (#180) (@viveksyngh)

#### CI:
  - Update kind github action to fix ci (#152) (@viveksyngh)
  - Remove travis ci config (#169) (@viveksyngh)

#### Helm:
  - Fix helm chart deprecated endpoints (#168) (@slimm609)
  - Update helm to helm3 in ci (#170) (@viveksyngh)
  - Adds support for SA annotations (#167) (@kkapoor1987)

#### Plugins:
  - Update ruby, fluentd, and gem plugins (#173) (@Cryptophobia)
      - Update fluentd gem to 1.11.2
      - Update ruby version to 2.7.2 (webrick CVE)
      - **DEPRECATION**: removing fluent-plugin-scribe as no longer maintained
  - Get vmware-log-intelligence from rubygems (#174) (@Cryptophobia)
      - Update fluent-plugin-vmware-log-intelligence to 2.0.5
  - Feat(splunk-hec): add plugin & fix dependencies (#179) (@jliao2011)
      - fluent-plugin-splunk-hec is added

## [1.14.0-beta.1](https://github.com/vmware/kube-fluentd-operator/releases/tag/v1.14.0-beta.1)

* Core: Expose config-reloader prometheus metrics (#147) (@tommasopozzetti )
* CI: Update github action to include kind test (#148) (@viveksyngh)
* Plugin: Update log intelligence plugin to 2.0.4 (#150) (@viveksyngh)

## [1.13.0](https://github.com/vmware/kube-fluentd-operator/releases/tag/v1.13.0)

* Core: Introduce 'crd' datasource (#111) (@tommasopozzetti )
* Helm: improve Helm chart and bump version to 0.3.4 (#130) (@dimalbaby )
* Core: Make the admin namespace configurable (#118 )(@tommasopozzetti )
* Helm: PriorityClassName and add ServiceMonitor in helm chart (#102)(@evilrussian )
* Image: Reduce image size (@dimalbaby )
* Core: Update CI github workflows (#129) (@tsunny )
* Plugin: Upgrade fluent-plugin-azure-loganalytics plugin (#136) (@floriankoch )

## [1.13.0-beta.2](https://github.com/vmware/kube-fluentd-operator/releases/tag/v1.13.0-beta.2)

* Helm: improve Helm chart and bump version to 0.3.4 (#130) (@dimalbaby )

## [1.13.0-beta.1](https://github.com/vmware/kube-fluentd-operator/releases/tag/v1.13.0-beta.1)

* Core: Introduce 'crd' datasource (#111) (@tommasopozzetti )
* Core: Make the admin namespace configurable (#118 )(@tommasopozzetti )
* Helm: PriorityClassName and add ServiceMonitor in helm chart (#102)(@evilrussian)
* Image: Reduce image size

## [1.12.0](https://github.com/vmware/kube-fluentd-operator/releases/tag/v1.12.0)

* Build kube-fluentd-operator on photon (#115) (@dimalbaby)

* Plugins: Add `fluent-plugin-vmware-loginsight` (@naveens)

* Plugins: Add `fluent-plugin-grafana-loki` (@SerialVelocity)

* Core: Cleanup unused namespace configuration files (#110) (@tommasopozzetti)

* Core: Fix labels not being rewritten in copy plugin (#86) (@tommasopozzetti)

* Core: Fix $label processor ignoring errors and not accepting "/" (#93) (@tommasopozzetti)

* Core: Fix namespace fluentd status annotation update (#92) (@tommasopozzetti)

* Core: Fix slow CRI-O log parsing (#91) (@jonasrutishauser)

* Core: Introduce a more efficient event-triggered reload system (#89)  (@tommasopozzetti)

* Core: Add new processor to allow controlled tag rewriting (#88) (@tommasopozzetti)

* Helm: improve Helm chart and bump version to 0.3.3 (#95) (@cablespaghetti)

* Fluentd: upgrade fluentd to 1.9.1

## [1.11.0](https://github.com/vmware/kube-fluentd-operator/releases/tag/v1.11.0)

* Plugins: Add `fluent-plugin-verticajson` again (@skalickym)

* Plugins: Add `fluent-plugin-uri-parser` (@rjackson90)

* Plugins: Add `fluent-plugin-out-http`

* Plugins: update to latest compatible versions

* Core: Efficient Kubernetes API Updates using Informers (#75) (@rjackson90)

* Fluend: Add support for CRI-O format (#80) (@jonasrutishauser)

## [1.10.0](https://github.com/vmware/kube-fluentd-operator/releases/tag/v1.10.0)

* Fluentd: Upgrade to 1.5.2

* Fluentd: Use libjemalloc from base image improving multi-platform build (@james-crowley)

* Plugins: Add `fluent-plugin-datadog` (@chirauki)

* Plugins: Add `fluent-plugin-multi-format-parser`

* Plugins: Add `fluent-plugin-json-in-json-2`

* Plugins: Add `fluent-plugin-gelf-hs`

* Plugins: Add `fluent-plugin-azure-loganalytics` (@zachomedia)

* Plugins: Upgrade LINT plugin to version 2.0.0

* Plugins: Remove vertica plugins as they fail to build with 1.5.2

* Core: `<plugin>`'s content is expanded correctly (#62) (@)

* Core: Allow the use of virtual `<plugin>` in store directive (#71) (@zachomedia)

* Core: Add subPath support to mounted-file (#63) (@jonasrutishauser)

## [1.9.0](https://github.com/vmware/kube-fluentd-operator/releases/tag/v1.9.0)

* Fluentd: BREAKING CHANGE: the plugin `fluent-plugin-parser` is not installed anymore. Instead the built-in `@type parser`
  is used and it has a different syntax (https://github.com/tagomoris/fluent-plugin-parser)

* Fluentd: Updated K8S integration to latest recommended for Fluentd 1.2.x

* Plugins: refresh all plugins to latest versions as of the release date.

* Plugins: add plugin `cloudwatch-logs` (@conradj87)

* Helm: improve Helm chart and bump version to 0.3.1 (@PabloCastellano)

## [1.8.0](https://github.com/vmware/kube-fluentd-operator/releases/tag/v1.8.0)

* Fluentd: replace fluent-plugin-amqp plugin with fluent-plugin-amqp2

* Fluentd: update fluentd to 1.2.6

* Fluentd: add plugin `fluent-plugin-vertica` to base image (@rhatlapa)

* Core configmaps per namespace support (#31) (@coufalja)

* Helm: chart updated to 0.3.0 adding support for multiple configmaps per namespace

## [1.7.0](https://github.com/vmware/kube-fluentd-operator/releases/tag/v1.7.0)

* Fluentd: add plugin `extract` to base image - a simple filter plugin to enrich log events based on regex and templates

* Fluentd: add plugin `fluent-plugin-amqp2` to base image (@CoufalJa)

* Fluentd: add plugin `fluent-plugin-grok-parser` to base image (@CoufalJa)

* Core: handle gracefully a missing `kubernetes.labels` field (#23)

* Core: Add `strict true|false` option to the logfmt parser plugin (#27)

* Core: Add `add_labels` to  `@type mounted_file` plug-in (#26)

* Core: Fix `@type mounted_file` for multi-container pods producing log files (#29)

* Helm: `podAnnotations` lets you annotate the daemonset pods (@cw-sakamoto) (#25)

## [1.6.0](https://github.com/vmware/kube-fluentd-operator/releases/tag/v1.6.0)

* Core: plugin macros (#19). This feature lets you reuse output plugin definitions.

* Fluentd: add `fluent-plugin-kafka` to base image (@dimitrovvlado)

* Fluentd: add `fluent-plugin-mail` to base image

* Fluentd: add `fluent-plugin-mongo` to base image

* Fluentd: add `fluent-plugin-scribe` to base image

* Fluentd: add `fluent-plugin-sumologic_output` to base image

## [1.5.0](https://github.com/vmware/kube-fluentd-operator/releases/tag/v1.5.0)

* Core: extreme validation (#15): namespace configs are run in sandbox to catch more errors

* Helm: export a K8S\_NODE\_NAME var to the fluentd container (@databus23)

* Helm: `extraEnv` lets you inject env vars into fluentd

## [1.4.0](https://github.com/vmware/kube-fluentd-operator/releases/tag/v1.4.0)

* Fluentd: add `fluent-plugin-kinesis` to base image (@anton-107)

## [1.3.0](https://github.com/vmware/kube-fluentd-operator/releases/tag/v1.3.0)

* Fluentd: add `fluent-plugin-detect-exceptions` to base image

* Fluentd: add `fluent-plugin-out-http-ext` to base image

* Core: add plugin `truncating_remote_syslog` which truncates the tag to 32 bytes as per RFC 5424

* Core: support transparent multi-line stacktrace collapsing

## [1.2.0](https://github.com/vmware/kube-fluentd-operator/releases/tag/v1.2.0)

* Core: Share log streams between namespaces

* Helm: Mount secrets/configmaps (tls mostly) ala elasticsearch (@sneko)

* Fluentd: Update base-image to fluentd-1.1.3-debian

* Fluentd: Include Splunk plugin into base-image (@mhulscher)

* Fix(Helm): properly set the `resources` field of the reloader container. Setting them had no effect until now (@sneko)

## [1.1.0](https://github.com/vmware/kube-fluentd-operator/releases/tag/v1.1.0)

* Core: ingest log files from a container filesystem

* Core: limit impact of log-router to a set of namespaces using `--namespaces`

* Helm: add new property `kubeletRoot`

* Helm: add new property `namespaces[]`:

## [1.0.1](https://github.com/vmware/kube-fluentd-operator/releases/tag/v1.0.1)

* Fluentd: install plugin `fluent-plugin-concat` in Fluentd

* Core: support for default configmap name using `--default-configmap`

## [1.0.0](https://github.com/vmware/kube-fluentd-operator/releases/tag/v1.0.0)

* Initial version
