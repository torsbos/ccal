# ccal
calcurse with smart updates and import deduplication, forked from https://github.com/jonhiggs/dedupe-calcurse-appointments

## features
- get updated appointments, notes and/or todos everytime `ccal` is invoked.
- import `.ics` files without duplicates, thanks to [jonhiggs dedupe-calcurse-appointments](https://github.com/jonhiggs/dedupe-calcurse-appointments).
- keep other appointments, notes or todos not specified in the `.ics` file intact.

## install
edit `c_dedupe` so the file path
```
CALCURSE_DIR=${CALCURSE_DIR:-${XDG_DATA_HOME}/calcurse}
```
matches your system - it must point to your `calcurse` folder.

then edit 
```
'https://example.url/file.ics'
```
in `ccal` so the url to your ics file is correct.

i suggest placing `ccal` in `/usr/local/bin` to be able to run `ccal` from anywhre on the system.

make `ccal` and `c_dedupe` executable:
```
chmod +x ccal c_dedupe
```
## usage
run `ccal` to start `calcurse` with updated data according to the `.ics` file - while still keeping other appointments, notes and todos intact.

another use case is to create an alias like this:
```
alias calcurse='ccal'

you can then run `calcurse` as normal, but with 
```

## dependencies
`curl`

`calcurse`
