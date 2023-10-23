
# Fn::
## Ref

- [[Parameters]] -> returns the value
- [[Resources]] -> returns the physical ID (e.g. [[EC2]] ID)

## GetAtt

Get the attributes of [[Resources]]
## FindInMap

Return a named value from a specific key in [[Mappings]]
`!FindInMap [MapName, TopLevelKey, SecondLevelKey]`
## ImportValue

Import values that are exported in other templates
## Join

![Fn::Join image by Stephane Maarek](https://github.com/devjiwonchoi/study-aws-sysops/blob/main/Screenshot%202023-10-23%20at%208.20.11%E2%80%AFPM.png?raw=true)
## Sub

Shorthand, is used to substitute variables

## [[Conditions]] Functions