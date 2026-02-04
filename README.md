## ccal
calcurse with import deduplication, forked from https://github.com/jonhiggs/dedupe-calcurse-appointments
`ccal` is able to import `.ics` files without duplicates and without overwriting other appointments, notes or todos.
# install
edit `c_dedupe` so the file path
```
CALCURSE_DIR=${CALCURSE_DIR:-${XDG_DATA_HOME}/calcurse}
```
matches your system.

then edit 
```
'https://example.url/file.ics'
```
in `ccal` so the url to your ics file is correct.

i suggest placing `ccal` in `/usr/local/bin`.

# usage
run `ccal` to get automatically update `calcurse` every time.

another use case is to create an alias like this:
```
alias calcurse='ccal'
```

# dependencies
`curl`
`calcurse`
