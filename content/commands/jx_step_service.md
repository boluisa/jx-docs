---
date: 2018-07-11T19:08:14Z
title: "jx step service"
slug: jx_step_service
url: /commands/jx_step_service/
---
## jx step service

achieve service linking in preview environments

### Synopsis

This pipeline step helps to link microservices from different namespaces like staging/production onto a preview environment

```
jx step service linking [flags]
```

### Examples

```
  #Link services from jx-staging namespace to the current namespace
  jx step link services --from-namespace jx-staging
  
  #Link services from jx-staging namespace to the jx-prod namespace
  jx step link services --from-namespace jx-staging --to-namespace jx-prod
  
  #Link services from jx-staging namespace to the jx-prod namespace including all but the ones starting with  the characters 'cheese'
  jx step link services --from-namespace jx-staging --to-namespace jx-prod --includes * --excludes cheese*
```

### Options

```
  -b, --batch-mode              In batch mode the command never prompts for user input
  -e, --excludes stringArray    What services from the source namespace to exclude from the linking process
  -f, --from-namespace string   The source namespace from which the linking would happen
      --headless                Enable headless operation if using browser automation
  -h, --help                    help for service
  -i, --includes stringArray    What services from source namespace to include in the linking process
      --no-brew                 Disables the use of brew on MacOS to install or upgrade command line dependencies
  -t, --to-namespace string     The destination namespace to which the linking would happen
      --verbose                 Enable verbose logging
```

### SEE ALSO

* [jx step](/commands/jx_step/)	 - pipeline steps

###### Auto generated by spf13/cobra on 11-Jul-2018
