![logo](http://eden.openovate.com/assets/images/cloud-social.png) Eden File
====
[![Build Status](https://api.travis-ci.org/Eden-PHP/File.svg)](https://travis-ci.org/Eden-PHP/File)
====

 - [Install](#install)
 - [Introduction](#intro)
 - [API](#api)
    - [isFile](#isFile)
    - [getBase](#getBase)
    - [getContent](#getContent)
    - [getData](#getData)
    - [getExtension](#getExtension)
    - [getFolder](#getFolder)
    - [getMime](#getMime)
    - [getName](#getName)
    - [getSize](#getSize)
    - [getTime](#getTime)
    - [setContent](#setContent)
    - [setData](#setData)
    - [remove](#remove)
    - [touch](#touch)
 - [Contributing](#contributing)

====

<a name="install"></a>
## Install

`composer install eden/file`

====

<a name="intro"></a>
## Introduction

Instantiate file in this manner.

```
$file = eden('file', '/some/path/to/file.txt');
```

====

<a name="api"></a>
## API

==== 

<a name="isFile"></a>

### isFile

Checks to see if this path is a real file 

#### Usage

```
eden('file', '/some/path/to/file.txt')->isFile();
```

#### Parameters

Returns `bool`

==== 

<a name="getBase"></a>

### getBase

Returns the base file name with out the extension 

#### Usage

```
eden('file', '/some/path/to/file.txt')->getBase();
```

#### Parameters

Returns `string`

==== 

<a name="getContent"></a>

### getContent

Returns the contents of a file given the path 

#### Usage

```
eden('file', '/some/path/to/file.txt')->getContent();
```

#### Parameters

Returns `string`

==== 

<a name="getData"></a>

### getData

Returns the executes the specified file and returns the final value 

#### Usage

```
eden('file', '/some/path/to/file.txt')->getData();
```

#### Parameters

Returns `bool`

==== 

<a name="getExtension"></a>

### getExtension

Returns the base file name extension 

#### Usage

```
eden('file', '/some/path/to/file.txt')->getExtension();
```

#### Parameters

Returns `string|null`

==== 

<a name="getFolder"></a>

### getFolder

Returns the file path 

#### Usage

```
eden('file', '/some/path/to/file.txt')->getFolder();
```

#### Parameters

Returns `string`

==== 

<a name="getMime"></a>

### getMime

Returns the mime type of a file 

#### Usage

```
eden('file', '/some/path/to/file.txt')->getMime();
```

#### Parameters

Returns `string`

==== 

<a name="getName"></a>

### getName

Returns the file name 

#### Usage

```
eden('file', '/some/path/to/file.txt')->getName();
```

#### Parameters

Returns `string`

==== 

<a name="getSize"></a>

### getSize

Returns the size of a file in bytes 

#### Usage

```
eden('file', '/some/path/to/file.txt')->getSize();
```

#### Parameters

Returns `string`

==== 

<a name="getTime"></a>

### getTime

Returns the last time file was modified in UNIX time 

#### Usage

```
eden('file', '/some/path/to/file.txt')->getTime();
```

#### Parameters

Returns `int`

==== 

<a name="setContent"></a>

### setContent

Creates a file and puts specified content into that file 

#### Usage

```
eden('file', '/some/path/to/file.txt')->setContent(*string $content);
```

#### Parameters

 - `*string $content` - The raw content to save

Returns `Eden\File\Index`

#### Example

```
eden('file', '/some/path/to/file.txt')->setContent('foo');
```

==== 

<a name="setData"></a>

### setData

Creates a php file and puts specified variable into that file 

#### Usage

```
eden('file', '/some/path/to/file.txt')->setData(*mixed $variable);
```

#### Parameters

 - `*mixed $variable` - Whatever data to save

Returns `Eden\File\Index`

#### Example

```
eden('file', '/some/path/to/file.txt')->setData($variable);
```

==== 

<a name="remove"></a>

### remove

Removes a file 

#### Usage

```
eden('file', '/some/path/to/file.txt')->remove();
```

#### Parameters

Returns `Eden\File\Index`

==== 

<a name="touch"></a>

### touch

Touches a file (effectively creates the file if it doesn't exist and updates the date if it does) 

#### Usage

```
eden('file', '/some/path/to/file.txt')->touch();
```

#### Parameters

Returns `Eden\File\Index`

==== 

<a name="contributing"></a>
#Contributing to Eden

Contributions to *Eden* are following the Github work flow. Please read up before contributing.

##Setting up your machine with the Eden repository and your fork

1. Fork the repository
2. Fire up your local terminal create a new branch from the `v4` branch of your 
fork with a branch name describing what your changes are. 
 Possible branch name types:
    - bugfix
    - feature
    - improvement
3. Make your changes. Always make sure to sign-off (-s) on all commits made (git commit -s -m "Commit message")

##Making pull requests

1. Please ensure to run `phpunit` before making a pull request.
2. Push your code to your remote forked version.
3. Go back to your forked version on GitHub and submit a pull request.
4. An Eden developer will review your code and merge it in when it has been classified as suitable.