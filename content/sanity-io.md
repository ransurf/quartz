---
title: Sanity io
---
Status: 
Tags: 
Links: [Coding MOC](out/coding-moc.md)
___

# Sanity io
## Principles
- Platform to store website content

### Setup
- On react root folder:
```
npm install -g @sanity/cli sanity init --coupon javascriptmastery2022
```
`npm i @sanity/client`

### Creating Schemas
- Create new exportable js file under schemas
- Import file in `schemas.js`, include in concat 

### Running
- Might need to solve [ps1 cannot be loaded](out/ps1-cannot-be-loaded.md)
- cd into right folder containing schemas
- `sanity start`
___
References:

Created:: 2022-02-28 09:32
