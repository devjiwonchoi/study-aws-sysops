
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

![[Screenshot 2023-10-23 at 8.20.11 PM.png]]
## Sub

Shorthand, is used to substitute variables

## [[Conditions]] Functions