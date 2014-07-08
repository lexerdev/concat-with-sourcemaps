## Concat with source maps

NPM module for concatenating text files and generating source maps.

### Usage example
```js
var concat = new Concat(true, 'all.js', '\n');
concat.add('file1.js', file1Content);
concat.add('file2.js', file2Content, file2SourceMap);

var concatenatedContent = concat.content;
var sourceMapForContent = concat.sourceMap;
```

### API

#### new Concat(generateSourceMap, outFileName, separator)
Initialize a new concat object.

Parameters:
- generateSourceMap: whether or not to generate a source map (default: false)
- outFileName: the file name/path of the output file (for the source map)
- separator: the string that should separate files (default: \n)

#### concat.add(fileName, content, sourceMap)
Add a file to the output file.

Parameters:
- fileName: file name of the input file
- content: content (string) of the input file
- sourceMap: optional source map of the input file. Will be merged into the output source map.

#### concat.content
The resulting concatenated file content.

#### concat.sourceMap
The resulting source map of the concatenated files.
