# README

Author: Lin Dong

Date: Mon Apr 20 12:23:57 PDT 2015,

## Notes

1. `git clone https://github.com/AloisReitbauer/w3cinpractice`

2. `node server.js` and http://localhost:3000/overview.html

## Timing

Guide line: [life cycle](http://w3.org/TR/resource-timing/):

1. Navigation Timing

2. Resource Timing

3. User Timing

### Resource Timing

It will measure the DOMs as the page loading, so we are good.

Collect information based on the domains

1. domain specific

2. easy to figure out which blocks the page loading

## Customize Header Tags

1. `Time-Allow-Origin` tag to see detailed information

## Cached Resource

1. Figure out if images are cached or not

## User Timing

Measuring JavaScript execution, it won't work with async/defer js.

Specific the priority of the loading

```html
<img src="..." prio="high" >
```

### Live Demo

New Specification have NOT been implemented yet:

1. Beacon, send analytics back to server

2. Network error logging, loading resource


### Page Visibility Example

## Contact Info
aloiseritbauer
alois.reitbauer@ruxit.com

