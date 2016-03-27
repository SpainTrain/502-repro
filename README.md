# Reproduction

1.  `./index.js` displays correctly
2.  `./some-dir/index.js` correctly displays `no-undef` error, but not `no-unused-vars` which should cascade
3.  run `npm run lint` to verify
4.  checkout c92e95d675da490cf089f0ebbb8b8f36cb30543d
5.  `./some-dir/index.js` correctly displays `no-undef` and `no-unused-vars`

There does appear to be some sensitivity to what file/project is open when Atom launches.  That is, it seem that opening a file in a different project (with eslint config file nesting) does not exhibit the errant behavior.
