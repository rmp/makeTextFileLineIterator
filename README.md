# makeTextFileLineIterator

This function is an almost-verbatim rip-off from https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch for reading a remote text file line by line.

Extended slightly to pass through fetch options. Specifically, I've used this with Range for fetching portions of remote FASTA files.

## Example Usage
```
    import makeTextFileLineIterator from 'makeTextFileLineIterator';

    for await (let line of makeTextFileLineIterator(urlOfFile)) {
        processLine(line);
    }
```