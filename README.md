# api documentation for  [parcelify (v2.2.0)](https://github.com/rotundasoftware/parcelify)  [![npm package](https://img.shields.io/npm/v/npmdoc-parcelify.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-parcelify) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-parcelify.svg)](https://travis-ci.org/npmdoc/node-npmdoc-parcelify)
#### Create css bundles from npm packages using the browserify dependency graph.

[![NPM](https://nodei.co/npm/parcelify.png?downloads=true)](https://www.npmjs.com/package/parcelify)

[![apidoc](https://npmdoc.github.io/node-npmdoc-parcelify/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-parcelify_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-parcelify/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-parcelify/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-parcelify/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Rotunda Software",
        "email": "support@rotundasoftware.com"
    },
    "bin": {
        "parcelify": "bin/cmd.js"
    },
    "bugs": {
        "url": "https://github.com/rotundasoftware/parcelify/issues"
    },
    "dependencies": {
        "async": "~0.2.10",
        "glob": "~3.2.9",
        "globwatcher": "~1.2.3",
        "inherits": "~2.0.1",
        "minimist": "0.0.8",
        "mkdirp": "~0.3.5",
        "npmlog": "0.0.6",
        "parcel-map": "^3.0.0",
        "resolve": "~0.6.1",
        "shasum": "~1.0.1",
        "stream-combiner": "^0.2.2",
        "through2": "~0.6.3",
        "toposort": "~0.2.10",
        "underscore": "~1.6.0"
    },
    "description": "Create css bundles from npm packages using the browserify dependency graph.",
    "devDependencies": {
        "browserify": "^9.0.8",
        "sass-css-stream": "^0.1.4",
        "tape": "~2.3.2"
    },
    "directories": {},
    "dist": {
        "shasum": "d77be17d13609e05e40f7409e1c4a162672c2391",
        "tarball": "https://registry.npmjs.org/parcelify/-/parcelify-2.2.0.tgz"
    },
    "gitHead": "5400f2a3faa960c712cad864e747ef0a42a0bd5a",
    "homepage": "https://github.com/rotundasoftware/parcelify",
    "keywords": [
        "parcel",
        "asset",
        "css",
        "commonjs",
        "browserify"
    ],
    "licenses": [
        {
            "type": "MIT",
            "url": "https://github.com/rotundasoftware/parcelify/blob/master/LICENSE"
        }
    ],
    "main": "index.js",
    "maintainers": [
        {
            "name": "rotundasoftware",
            "email": "oleg@rotundasoftware.com"
        },
        {
            "name": "go-oleg",
            "email": "oleg.b.seletsky@gmail.com"
        },
        {
            "name": "davidbeck",
            "email": "david@rotundasoftware.com"
        },
        {
            "name": "substack",
            "email": "mail@substack.net"
        }
    ],
    "name": "parcelify",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/rotundasoftware/parcelify.git"
    },
    "scripts": {
        "test": "tape test/test.js"
    },
    "version": "2.2.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module parcelify](#apidoc.module.parcelify)
1.  [function <span class="apidocSignatureSpan">parcelify.</span>package ( options )](#apidoc.element.parcelify.package)
1.  [function <span class="apidocSignatureSpan">parcelify.</span>parcel ( options )](#apidoc.element.parcelify.parcel)
1.  [function <span class="apidocSignatureSpan">parcelify.</span>super_ ()](#apidoc.element.parcelify.super_)
1.  object <span class="apidocSignatureSpan">parcelify.</span>package.prototype
1.  object <span class="apidocSignatureSpan">parcelify.</span>parcel.prototype

#### [module parcelify.package](#apidoc.module.parcelify.package)
1.  [function <span class="apidocSignatureSpan">parcelify.</span>package ( options )](#apidoc.element.parcelify.package.package)
1.  [function <span class="apidocSignatureSpan">parcelify.package.</span>getOptionsFromPackageJson ( packageId, packagePath, packageJson, assetTypes, appTransforms, appTransformDirs, callback )](#apidoc.element.parcelify.package.getOptionsFromPackageJson)
1.  [function <span class="apidocSignatureSpan">parcelify.package.</span>super_ ()](#apidoc.element.parcelify.package.super_)

#### [module parcelify.package.prototype](#apidoc.module.parcelify.package.prototype)
1.  [function <span class="apidocSignatureSpan">parcelify.package.prototype.</span>_createAssetGlobWatchers ()](#apidoc.element.parcelify.package.prototype._createAssetGlobWatchers)
1.  [function <span class="apidocSignatureSpan">parcelify.package.prototype.</span>_createPackageJsonWatcher ( assetTypes, packageFilter, appTransforms, appTransformDirs )](#apidoc.element.parcelify.package.prototype._createPackageJsonWatcher)
1.  [function <span class="apidocSignatureSpan">parcelify.package.prototype.</span>_destroyAssetGlobWatchers ()](#apidoc.element.parcelify.package.prototype._destroyAssetGlobWatchers)
1.  [function <span class="apidocSignatureSpan">parcelify.package.prototype.</span>_emitEventOnRelevantParcels ()](#apidoc.element.parcelify.package.prototype._emitEventOnRelevantParcels)
1.  [function <span class="apidocSignatureSpan">parcelify.package.prototype.</span>addDependentParcel ( parcel )](#apidoc.element.parcelify.package.prototype.addDependentParcel)
1.  [function <span class="apidocSignatureSpan">parcelify.package.prototype.</span>addTransform ( transform, transformOptions, toAssetTypes, prepend )](#apidoc.element.parcelify.package.prototype.addTransform)
1.  [function <span class="apidocSignatureSpan">parcelify.package.prototype.</span>createAllAssets ( assetTypes )](#apidoc.element.parcelify.package.prototype.createAllAssets)
1.  [function <span class="apidocSignatureSpan">parcelify.package.prototype.</span>createAsset ( thisAssetSrcPath, assetType, appData )](#apidoc.element.parcelify.package.prototype.createAsset)
1.  [function <span class="apidocSignatureSpan">parcelify.package.prototype.</span>createWatchers ( assetTypes, packageFilter, appTransforms, appTransformDirs )](#apidoc.element.parcelify.package.prototype.createWatchers)
1.  [function <span class="apidocSignatureSpan">parcelify.package.prototype.</span>destroy ()](#apidoc.element.parcelify.package.prototype.destroy)
1.  [function <span class="apidocSignatureSpan">parcelify.package.prototype.</span>getAssets ( types )](#apidoc.element.parcelify.package.prototype.getAssets)
1.  [function <span class="apidocSignatureSpan">parcelify.package.prototype.</span>setDependencies ( dependencies )](#apidoc.element.parcelify.package.prototype.setDependencies)

#### [module parcelify.parcel](#apidoc.module.parcelify.parcel)
1.  [function <span class="apidocSignatureSpan">parcelify.</span>parcel ( options )](#apidoc.element.parcelify.parcel.parcel)
1.  [function <span class="apidocSignatureSpan">parcelify.parcel.</span>super_ ( options )](#apidoc.element.parcelify.parcel.super_)

#### [module parcelify.parcel.prototype](#apidoc.module.parcelify.parcel.prototype)
1.  [function <span class="apidocSignatureSpan">parcelify.parcel.prototype.</span>attachWatchListeners ( bundles )](#apidoc.element.parcelify.parcel.prototype.attachWatchListeners)
1.  [function <span class="apidocSignatureSpan">parcelify.parcel.prototype.</span>calcParcelAssets ( assetTypes )](#apidoc.element.parcelify.parcel.prototype.calcParcelAssets)
1.  [function <span class="apidocSignatureSpan">parcelify.parcel.prototype.</span>calcSortedDependencies ()](#apidoc.element.parcelify.parcel.prototype.calcSortedDependencies)
1.  [function <span class="apidocSignatureSpan">parcelify.parcel.prototype.</span>writeBundle ( assetType, dstPath, callback )](#apidoc.element.parcelify.parcel.prototype.writeBundle)



# <a name="apidoc.module.parcelify"></a>[module parcelify](#apidoc.module.parcelify)

#### <a name="apidoc.element.parcelify.package"></a>[function <span class="apidocSignatureSpan">parcelify.</span>package ( options )](#apidoc.element.parcelify.package)
- description and source-code
```javascript
function Package( options ) {

	_.extend( this, _.pick( options,
		'id',
		'package',
		'path',
		'dependencies',
		'assetSrcPathsByType',
		'assetGlobsByType',
		'assetTransformsByType'
	) );

	this.dependencies = [];
	this.dependentParcels = [];
	this.assetsByType = {};

	EventEmitter.call( this );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parcelify.parcel"></a>[function <span class="apidocSignatureSpan">parcelify.</span>parcel ( options )](#apidoc.element.parcelify.parcel)
- description and source-code
```javascript
function Parcel( options ) {
	var _this = this;

	Package.call( this, options );

	this.mainPath = options.mainPath;
	this.isParcel = true;
	this.bundlePathsByType = {};
	this.parcelAssetsByType = {};

	this.dependentParcels.push( this ); // parcels depend on themselves!
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parcelify.super_"></a>[function <span class="apidocSignatureSpan">parcelify.</span>super_ ()](#apidoc.element.parcelify.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.parcelify.package"></a>[module parcelify.package](#apidoc.module.parcelify.package)

#### <a name="apidoc.element.parcelify.package.package"></a>[function <span class="apidocSignatureSpan">parcelify.</span>package ( options )](#apidoc.element.parcelify.package.package)
- description and source-code
```javascript
function Package( options ) {

	_.extend( this, _.pick( options,
		'id',
		'package',
		'path',
		'dependencies',
		'assetSrcPathsByType',
		'assetGlobsByType',
		'assetTransformsByType'
	) );

	this.dependencies = [];
	this.dependentParcels = [];
	this.assetsByType = {};

	EventEmitter.call( this );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parcelify.package.getOptionsFromPackageJson"></a>[function <span class="apidocSignatureSpan">parcelify.package.</span>getOptionsFromPackageJson ( packageId, packagePath, packageJson, assetTypes, appTransforms, appTransformDirs, callback )](#apidoc.element.parcelify.package.getOptionsFromPackageJson)
- description and source-code
```javascript
getOptionsFromPackageJson = function ( packageId, packagePath, packageJson, assetTypes, appTransforms, appTransformDirs, callback ) {
	var packageOptions = {};

	if( appTransforms ) {
		var pkgIsInAppTransformsDir = _.find( appTransformDirs, function( thisAppDirPath ) {
			var relPath = path.relative( thisAppDirPath, packagePath );
			var needToBackup = relPath.charAt( 0 ) === '.' && relPath.charAt( 1 ) === '.';
			var appTransformsApplyToThisDir = ! needToBackup && relPath.indexOf( 'node_modules' ) === -1;
			return appTransformsApplyToThisDir;
		} );

		if( pkgIsInAppTransformsDir )
			packageJson.transforms = appTransforms.concat( packageJson.transforms || [] );
	}

	packageOptions.package = packageJson;
	packageOptions.id = packageId;
	packageOptions.path = packagePath;

	packageOptions.assetSrcPathsByType = {};
	packageOptions.assetTransformsByType = {};
	packageOptions.assetGlobsByType = {};

	async.each( assetTypes, function( thisAssetType, nextAssetType ) {

		async.parallel( [ function( nextParallel ) {
			packageOptions.assetSrcPathsByType[ thisAssetType ] = [];

			// resolve relative globs to absolute globs
			var relativeGlobsOfThisType = packageJson[ thisAssetType ] || [];
			if( _.isString( relativeGlobsOfThisType ) ) relativeGlobsOfThisType = [ relativeGlobsOfThisType ];
			var absoluteGlobsOfThisType = relativeGlobsOfThisType.map( function( thisGlob ) { return path.resolve( packagePath, thisGlob ); } );
			packageOptions.assetGlobsByType[ thisAssetType ] = absoluteGlobsOfThisType;

			// resolve absolute globs to actual src files
			async.map( absoluteGlobsOfThisType, glob,
			function( err, arrayOfResolvedGlobs ) {
				if( err ) return nextParallel( err );

				var assetsOfThisType = _.flatten( arrayOfResolvedGlobs );
				packageOptions.assetSrcPathsByType[ thisAssetType ] = assetsOfThisType;

				nextParallel();
			} );
		}, function( nextParallel ) {
			// resolve transform names to actual transform
			packageOptions.assetTransformsByType[ thisAssetType ] = [];

			if( packageJson.transforms ) {
				if( _.isArray( packageJson.transforms ) )
					transformNames = packageJson.transforms;
				else
					transformNames = packageJson.transforms[ thisAssetType ] || [];
			}
			else
				transformNames = [];

			async.map( transformNames, function( thisTransformName, nextTransform ) {
				if( _.isFunction( thisTransformName ) ) return nextTransform( null, thisTransformName );

				resolve( thisTransformName, { basedir : packageJson.__path }, function( err, modulePath ) {
					if( err ) return nextTransform( err );

					nextTransform( null, require( modulePath ) );
				} );
			}, function( err, transforms ) {
				if( err ) return nextParallel( err );


				packageOptions.assetTransformsByType[ thisAssetType ] = transforms;
				nextParallel();
			} );
		} ], nextAssetType );
	}, function( err ) {
		if( err ) return callback( err );

		callback( null, packageOptions );
	} );
}
```
- example usage
```shell
...

	async.series( [ function( nextSeries ) {
		async.each( Object.keys( parcelMapResult.packages ), function( thisPackageId, nextPackageId ) {
			var packageJson = parcelMapResult.packages[ thisPackageId ];
			var packageOptions = {};

			async.waterfall( [ function( nextWaterfall ) {
				Package.getOptionsFromPackageJson( thisPackageId, packageJson.__path, packageJson, assetTypes, appTransforms, appTransformDirs
, nextWaterfall );
			}, function( packageOptions, nextWaterfall ) {
				var thisPackage;

				var thisPackageIsAParcel = packageJson.__isParcel;

				if( ! existingPacakages[ thisPackageId ] ) {
					if( thisPackageIsAParcel ) {
...
```

#### <a name="apidoc.element.parcelify.package.super_"></a>[function <span class="apidocSignatureSpan">parcelify.package.</span>super_ ()](#apidoc.element.parcelify.package.super_)
- description and source-code
```javascript
function EventEmitter() {
  EventEmitter.init.call(this);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.parcelify.package.prototype"></a>[module parcelify.package.prototype](#apidoc.module.parcelify.package.prototype)

#### <a name="apidoc.element.parcelify.package.prototype._createAssetGlobWatchers"></a>[function <span class="apidocSignatureSpan">parcelify.package.prototype.</span>_createAssetGlobWatchers ()](#apidoc.element.parcelify.package.prototype._createAssetGlobWatchers)
- description and source-code
```javascript
_createAssetGlobWatchers = function () {
	var _this = this;

	this.assetGlobWatchers = [];

	_.each( _this.assetGlobsByType, function( globs, thisAssetType ) {
		var thisWatcher = globwatcher( globs );

		thisWatcher.on( 'changed', function( srcPath ) {
			try {
				log.info( 'watch', '"%s" changed', path.relative( process.cwd(), srcPath ) );

				var asset = _.findWhere( _this.assetsByType[ thisAssetType ], { srcPath : srcPath } );
				if( ! asset ) return _this.emit( 'error', new Error( 'Couldn\'t find changed file ' + srcPath + ' in assets of type ' + thisAssetType
 ) );

				_this._emitEventOnRelevantParcels( 'assetUpdated', 'changed', asset, _this );
			} catch( err ) {
				return _this.emit( 'error', err );
			}
		} );

		thisWatcher.on( 'added', function( srcPath ) {
			try {
				log.info( 'watch', '"%s" added', path.relative( process.cwd(), srcPath ) );
			
				var asset = _.findWhere( _this.assetsByType[ thisAssetType ], { srcPath : srcPath } );
				// watching is weird... sometimes we get double events. make sure we don't add the same asset twice.
				if( asset ) return _this.emit( 'error', new Error( 'Asset ' + srcPath + ' already exists in assets of type ' + thisAssetType
 ) );
				
				asset = _this.createAsset( srcPath, thisAssetType );

				_this._emitEventOnRelevantParcels( 'assetUpdated', 'added', asset, _this );
			} catch( err ) {
				return _this.emit( 'error', err );
			}
		} );

		thisWatcher.on( 'deleted', function( srcPath ) {
			try {
				log.info( 'watch', '"%s" deleted', path.relative( process.cwd(), srcPath ) );

				var asset = _.findWhere( _this.assetsByType[ thisAssetType ], { srcPath : srcPath } );
				if( ! asset ) return _this.emit( 'error', new Error( 'Couldn\'t find changed file ' + srcPath + ' in assets of type ' + thisAssetType
 ) );

				_this.assetsByType[ thisAssetType ] = _.without( _this.assetsByType[ thisAssetType ], asset );
			
				_this._emitEventOnRelevantParcels( 'assetUpdated', 'deleted', asset, _this );
			} catch( err ) {
				return _this.emit( 'error', err );
			}
		} );

		_this.assetGlobWatchers.push( thisWatcher );
	} );
}
```
- example usage
```shell
...

Package.prototype.addDependentParcel = function( parcel ) {
	this.dependentParcels = _.union( this.dependentParcels, parcel );
};

Package.prototype.createWatchers = function( assetTypes, packageFilter, appTransforms, appTransformDirs ) {
	this._createPackageJsonWatcher( assetTypes, packageFilter, appTransforms, appTransformDirs );
	this._createAssetGlobWatchers();
};

Package.prototype.destroy = function() {
	this._destroyAssetGlobWatchers();
	this.assetJsonWatcher.close();
};
...
```

#### <a name="apidoc.element.parcelify.package.prototype._createPackageJsonWatcher"></a>[function <span class="apidocSignatureSpan">parcelify.package.prototype.</span>_createPackageJsonWatcher ( assetTypes, packageFilter, appTransforms, appTransformDirs )](#apidoc.element.parcelify.package.prototype._createPackageJsonWatcher)
- description and source-code
```javascript
_createPackageJsonWatcher = function ( assetTypes, packageFilter, appTransforms, appTransformDirs ) {
	var _this = this;

	this.assetJsonWatcher = globwatcher( path.resolve( this.path, "package.json" ) );
	this.assetJsonWatcher.on( 'changed', function( srcPath ) {
		log.info( 'watch', 'package.json changed "%s"', path.relative( process.cwd(), srcPath ) );

		fs.readFile( srcPath, 'utf8', function( err, packageJson ) {
			if( err ) return _this.emit( 'error', err );

			try {
				packageJson = JSON.parse( packageJson );
			} catch( err ) {
				return _this.emit( 'error', new Error( 'While parsing "' + srcPath + '", ' + err ) );
			}

			packageJson.__path = _this.path;

			if( packageFilter ) packageJson = packageFilter( packageJson, _this.path );

			Package.getOptionsFromPackageJson( _this.id, _this.path, packageJson, assetTypes, appTransforms, appTransformDirs, function(
err, options ) {
				if( err ) return _this.emit( 'error', err );

				_.extend( _this, options );

				_this.createAllAssets( assetTypes );

				_this._destroyAssetGlobWatchers();
				_this._createAssetGlobWatchers();

				_this._emitEventOnRelevantParcels( 'packageJsonUpdated', _this );
			} );
		} );
	} );
}
```
- example usage
```shell
...
};

Package.prototype.addDependentParcel = function( parcel ) {
	this.dependentParcels = _.union( this.dependentParcels, parcel );
};

Package.prototype.createWatchers = function( assetTypes, packageFilter, appTransforms, appTransformDirs ) {
	this._createPackageJsonWatcher( assetTypes, packageFilter, appTransforms, appTransformDirs );
	this._createAssetGlobWatchers();
};

Package.prototype.destroy = function() {
	this._destroyAssetGlobWatchers();
	this.assetJsonWatcher.close();
};
...
```

#### <a name="apidoc.element.parcelify.package.prototype._destroyAssetGlobWatchers"></a>[function <span class="apidocSignatureSpan">parcelify.package.prototype.</span>_destroyAssetGlobWatchers ()](#apidoc.element.parcelify.package.prototype._destroyAssetGlobWatchers)
- description and source-code
```javascript
_destroyAssetGlobWatchers = function () {
	this.assetGlobWatchers.forEach( function( thisAssetGlobWatcher ) {
		thisAssetGlobWatcher.close();
	} );

	this.assetGlobWatchers = [];
}
```
- example usage
```shell
...

Package.prototype.createWatchers = function( assetTypes, packageFilter, appTransforms, appTransformDirs ) {
	this._createPackageJsonWatcher( assetTypes, packageFilter, appTransforms, appTransformDirs );
	this._createAssetGlobWatchers();
};

Package.prototype.destroy = function() {
	this._destroyAssetGlobWatchers();
	this.assetJsonWatcher.close();
};

/********************* Private instance methods *********************/

Package.prototype._createPackageJsonWatcher = function( assetTypes, packageFilter, appTransforms, appTransformDirs ) {
	var _this = this;
...
```

#### <a name="apidoc.element.parcelify.package.prototype._emitEventOnRelevantParcels"></a>[function <span class="apidocSignatureSpan">parcelify.package.prototype.</span>_emitEventOnRelevantParcels ()](#apidoc.element.parcelify.package.prototype._emitEventOnRelevantParcels)
- description and source-code
```javascript
_emitEventOnRelevantParcels = function () {
	var args = Array.prototype.slice.call( arguments );

	this.dependentParcels.forEach( function( thisParcel ) {
		thisParcel.emit.apply( thisParcel, args );
	} );
}
```
- example usage
```shell
...
				_.extend( _this, options );

				_this.createAllAssets( assetTypes );

				_this._destroyAssetGlobWatchers();
				_this._createAssetGlobWatchers();

				_this._emitEventOnRelevantParcels( 'packageJsonUpdated', _this );
			} );
		} );
	} );
};

Package.prototype._createAssetGlobWatchers = function() {
	var _this = this;
...
```

#### <a name="apidoc.element.parcelify.package.prototype.addDependentParcel"></a>[function <span class="apidocSignatureSpan">parcelify.package.prototype.</span>addDependentParcel ( parcel )](#apidoc.element.parcelify.package.prototype.addDependentParcel)
- description and source-code
```javascript
addDependentParcel = function ( parcel ) {
	this.dependentParcels = _.union( this.dependentParcels, parcel );
}
```
- example usage
```shell
...

					oldPackage.destroy();

					thisPackage = packagesThatWereCreated[ thisPackageId ] = new Parcel( packageOptions );
					thisPackage.createAllAssets( assetTypes );

					oldDependentParcels.forEach( function( thisDependentParcel ) {
						thisPackage.addDependentParcel( thisDependentParcel );
						thisDependentParcel.calcSortedDependencies();
						thisDependentParcel.calcParcelAssets( assetTypes );
					} );

					log.warn( '', 'Recreated package at ' + thisPackage.path + ' as Parcel.' );
				} else
					thisPackage = existingPacakages[ thisPackageId ];
...
```

#### <a name="apidoc.element.parcelify.package.prototype.addTransform"></a>[function <span class="apidocSignatureSpan">parcelify.package.prototype.</span>addTransform ( transform, transformOptions, toAssetTypes, prepend )](#apidoc.element.parcelify.package.prototype.addTransform)
- description and source-code
```javascript
addTransform = function ( transform, transformOptions, toAssetTypes, prepend ) {
	if( _.isUndefined( prepend ) ) prepend = false;

	var t = transformOptions ? function( file ) { return transform( file, transformOptions ); } : transform;

	toAssetTypes = toAssetTypes || Object.keys( this.assetsByType );
	if( ! _.isArray( toAssetTypes ) ) toAssetTypes = [ toAssetTypes ];

	// add transform to existing assets
	this.getAssets( toAssetTypes ).forEach( function( thisAsset ) {
		thisAsset.addTransform( t, prepend );
	} );

	// and also add it to the package itself so it is added to assets created from this point forward
	_.each( _.pick( this.assetTransformsByType, toAssetTypes ), function( transformsForThisAssetType ) {
		if( prepend ) transformsForThisAssetType.unshift( t );
		else transformsForThisAssetType.push( t );
	} );
}
```
- example usage
```shell
...
	var t = transformOptions ? function( file ) { return transform( file, transformOptions ); } : transform;

	toAssetTypes = toAssetTypes || Object.keys( this.assetsByType );
	if( ! _.isArray( toAssetTypes ) ) toAssetTypes = [ toAssetTypes ];

	// add transform to existing assets
	this.getAssets( toAssetTypes ).forEach( function( thisAsset ) {
		thisAsset.addTransform( t, prepend );
	} );

	// and also add it to the package itself so it is added to assets created from this point forward
	_.each( _.pick( this.assetTransformsByType, toAssetTypes ), function( transformsForThisAssetType ) {
		if( prepend ) transformsForThisAssetType.unshift( t );
		else transformsForThisAssetType.push( t );
	} );
...
```

#### <a name="apidoc.element.parcelify.package.prototype.createAllAssets"></a>[function <span class="apidocSignatureSpan">parcelify.package.prototype.</span>createAllAssets ( assetTypes )](#apidoc.element.parcelify.package.prototype.createAllAssets)
- description and source-code
```javascript
createAllAssets = function ( assetTypes ) {
	var _this = this;

	_this.assetsByType = {};
	assetTypes.forEach( function( thisAssetType ) { _this.assetsByType[ thisAssetType ] = []; } );

	Object.keys( this.assetSrcPathsByType ).forEach( function( assetType ) {
		_this.assetSrcPathsByType[ assetType ].forEach( function( thisAssetSrcPath ) {
			var thisAsset = _this.createAsset( thisAssetSrcPath, assetType );
		} );
	} );
}
```
- example usage
```shell
...

				if( ! existingPacakages[ thisPackageId ] ) {
					if( thisPackageIsAParcel ) {
						thisPackage = packagesThatWereCreated[ thisPackageId ] = new Parcel( _.extend( packageOptions, { mainPath : packageJson.__mainPath
 } ) );
					}
					else thisPackage = packagesThatWereCreated[ thisPackageId ] = new Package( packageOptions );

					thisPackage.createAllAssets( assetTypes );
				}
				else if( thisPackageIsAParcel && ! existingPacakages[ thisPackageId ] instanceof Parcel ) {
					// k tricky here.. if this package is a parcel, but it exists in the manifest as a plain
					// old package, then we gotta recreate this package as a parcel. also we have to update
					// any parcels that are dependENTS of this package/parcel in order to use the new
					// assets that we are about to create. man, scary, hope nothing gets broke in the process.
					// we could also pre-preemptively list out which packages are parcels by adding an option
...
```

#### <a name="apidoc.element.parcelify.package.prototype.createAsset"></a>[function <span class="apidocSignatureSpan">parcelify.package.prototype.</span>createAsset ( thisAssetSrcPath, assetType, appData )](#apidoc.element.parcelify.package.prototype.createAsset)
- description and source-code
```javascript
createAsset = function ( thisAssetSrcPath, assetType, appData ) {
	var thisAsset = new Asset( thisAssetSrcPath, assetType, _.clone( this.assetTransformsByType[ assetType ] ), appData );

	log.verbose( '', assetType + ' asset registered "%s"', path.relative( process.cwd(), thisAssetSrcPath ) );

	if( ! this.assetsByType[ assetType ] ) this.assetsByType[ assetType ] = [];
	this.assetsByType[ assetType ].push( thisAsset );

	return thisAsset;
}
```
- example usage
```shell
...
	var _this = this;

	_this.assetsByType = {};
	assetTypes.forEach( function( thisAssetType ) { _this.assetsByType[ thisAssetType ] = []; } );

	Object.keys( this.assetSrcPathsByType ).forEach( function( assetType ) {
		_this.assetSrcPathsByType[ assetType ].forEach( function( thisAssetSrcPath ) {
			var thisAsset = _this.createAsset( thisAssetSrcPath, assetType );
		} );
	} );
};

Package.prototype.createAsset = function( thisAssetSrcPath, assetType, appData ) {
	var thisAsset = new Asset( thisAssetSrcPath, assetType, _.clone( this.assetTransformsByType[ assetType ] ), appData );
...
```

#### <a name="apidoc.element.parcelify.package.prototype.createWatchers"></a>[function <span class="apidocSignatureSpan">parcelify.package.prototype.</span>createWatchers ( assetTypes, packageFilter, appTransforms, appTransformDirs )](#apidoc.element.parcelify.package.prototype.createWatchers)
- description and source-code
```javascript
createWatchers = function ( assetTypes, packageFilter, appTransforms, appTransformDirs ) {
	this._createPackageJsonWatcher( assetTypes, packageFilter, appTransforms, appTransformDirs );
	this._createAssetGlobWatchers();
}
```
- example usage
```shell
...
						}, nextEach );
					}, nextSeries );
				}, function( nextSeries ) {
					if( options.watch ) {
						// we only create glob watchers for the packages that parcel added to the manifest. Again, we want to avoid doubling up
						// work in situations where we have multiple parcelify instances running that share common bundles
						_.each( packagesThatWereCreated, function( thisPackage ) {
							thisPackage.createWatchers( assetTypes, browserifyInstance._options.packageFilter, options.appTransforms, options.appTransformDirs
 );
							if( thisPackage.isParcel ) {
								thisPackage.attachWatchListeners( options.bundlesByEntryPoint[ thisPackage.mainPath ] );
							}
						} );
					}

					if( ! _this.watching ) _this.emit( 'done' );
...
```

#### <a name="apidoc.element.parcelify.package.prototype.destroy"></a>[function <span class="apidocSignatureSpan">parcelify.package.prototype.</span>destroy ()](#apidoc.element.parcelify.package.prototype.destroy)
- description and source-code
```javascript
destroy = function () {
	this._destroyAssetGlobWatchers();
	this.assetJsonWatcher.close();
}
```
- example usage
```shell
...
					// assets that we are about to create. man, scary, hope nothing gets broke in the process.
					// we could also pre-preemptively list out which packages are parcels by adding an option
					// to parcelify itself, but that seems a little weird. In the context of cartero that
					// depends on the path of each package relative to the parcelDirs cartero option.
					var oldPackage = existingPacakages[ thisPackageId ];
					var oldDependentParcels = oldPackage.dependentParcels;

					oldPackage.destroy();

					thisPackage = packagesThatWereCreated[ thisPackageId ] = new Parcel( packageOptions );
					thisPackage.createAllAssets( assetTypes );

					oldDependentParcels.forEach( function( thisDependentParcel ) {
						thisPackage.addDependentParcel( thisDependentParcel );
						thisDependentParcel.calcSortedDependencies();
...
```

#### <a name="apidoc.element.parcelify.package.prototype.getAssets"></a>[function <span class="apidocSignatureSpan">parcelify.package.prototype.</span>getAssets ( types )](#apidoc.element.parcelify.package.prototype.getAssets)
- description and source-code
```javascript
getAssets = function ( types ) {
	return _.reduce( this.assetsByType, function( memo, assetsOfThisType, thisAssetType ) {
		if( types && ! _.contains( types, thisAssetType ) ) return memo;

		return memo.concat( assetsOfThisType );
	}, [] );
}
```
- example usage
```shell
...

	var t = transformOptions ? function( file ) { return transform( file, transformOptions ); } : transform;

	toAssetTypes = toAssetTypes || Object.keys( this.assetsByType );
	if( ! _.isArray( toAssetTypes ) ) toAssetTypes = [ toAssetTypes ];

	// add transform to existing assets
	this.getAssets( toAssetTypes ).forEach( function( thisAsset ) {
		thisAsset.addTransform( t, prepend );
	} );

	// and also add it to the package itself so it is added to assets created from this point forward
	_.each( _.pick( this.assetTransformsByType, toAssetTypes ), function( transformsForThisAssetType ) {
		if( prepend ) transformsForThisAssetType.unshift( t );
		else transformsForThisAssetType.push( t );
...
```

#### <a name="apidoc.element.parcelify.package.prototype.setDependencies"></a>[function <span class="apidocSignatureSpan">parcelify.package.prototype.</span>setDependencies ( dependencies )](#apidoc.element.parcelify.package.prototype.setDependencies)
- description and source-code
```javascript
setDependencies = function ( dependencies ) {
	this.dependencies = dependencies;
}
```
- example usage
```shell
...
		// now that we have all our packages instantiated, hook up dependencies
		_.each( parcelMapResult.dependencies, function( dependencyIds, thisPackageId ) {
			var thisPackage = allPackages[ thisPackageId ];

			if( ! thisPackage ) return nextSeries( new Error( 'Unknown package id in dependency ' + thisPackageId ) );

			var thisPackageDependencies = _.map( dependencyIds, function( thisDependencyId ) { return allPackages[ thisDependencyId ]; } );
			thisPackage.setDependencies( thisPackageDependencies );
		} );

		// finally, we can calculate the topo sort of any parcels that were created
		_.each( packagesThatWereCreated, function( thisParcel ) {
			if( thisParcel.isParcel ) {
				thisParcel.calcSortedDependencies();
				thisParcel.calcParcelAssets( assetTypes );
...
```



# <a name="apidoc.module.parcelify.parcel"></a>[module parcelify.parcel](#apidoc.module.parcelify.parcel)

#### <a name="apidoc.element.parcelify.parcel.parcel"></a>[function <span class="apidocSignatureSpan">parcelify.</span>parcel ( options )](#apidoc.element.parcelify.parcel.parcel)
- description and source-code
```javascript
function Parcel( options ) {
	var _this = this;

	Package.call( this, options );

	this.mainPath = options.mainPath;
	this.isParcel = true;
	this.bundlePathsByType = {};
	this.parcelAssetsByType = {};

	this.dependentParcels.push( this ); // parcels depend on themselves!
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.parcelify.parcel.super_"></a>[function <span class="apidocSignatureSpan">parcelify.parcel.</span>super_ ( options )](#apidoc.element.parcelify.parcel.super_)
- description and source-code
```javascript
function Package( options ) {

	_.extend( this, _.pick( options,
		'id',
		'package',
		'path',
		'dependencies',
		'assetSrcPathsByType',
		'assetGlobsByType',
		'assetTransformsByType'
	) );

	this.dependencies = [];
	this.dependentParcels = [];
	this.assetsByType = {};

	EventEmitter.call( this );
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.parcelify.parcel.prototype"></a>[module parcelify.parcel.prototype](#apidoc.module.parcelify.parcel.prototype)

#### <a name="apidoc.element.parcelify.parcel.prototype.attachWatchListeners"></a>[function <span class="apidocSignatureSpan">parcelify.parcel.prototype.</span>attachWatchListeners ( bundles )](#apidoc.element.parcelify.parcel.prototype.attachWatchListeners)
- description and source-code
```javascript
attachWatchListeners = function ( bundles ) {
	var _this = this;

	this.on( 'assetUpdated', function( eventType, asset ) {
		if( _.contains( [ 'added', 'deleted' ], eventType ) )
			this.calcParcelAssets( [ asset.type ] );

		if( bundles[ asset.type ] ) {
			_this.writeBundle( asset.type, bundles[ asset.type ], function( err, bundleWasWritten ) {
				if( err ) return _this.emit( 'error', err );

				if( bundleWasWritten ) _this.emit( 'bundleUpdated', bundles[ asset.type ], asset.type );
				// ... done!
			} );
		}
	} );

	this.on( 'packageJsonUpdated', function( thePackage ) {
		var bundlesToRewrite = _.pick( bundles, _.without( Object.keys( bundles ), 'script' ) );
		this.calcParcelAssets( Object.keys( bundlesToRewrite ) );

		async.each( Object.keys( bundlesToRewrite ), function( thisAssetType, nextEach ) {
			var thisBundlePath = bundlesToRewrite[ thisAssetType ];
			if( ! thisBundlePath ) return nextEach();
		
			_this.writeBundle( thisAssetType, thisBundlePath, function( err, bundleWasWritten ) {
				// don't stop writing other bundles if there was an error on this one. errors happen
				// frequently with transforms.. like invalid scss, etc. don't stop the show, just
				// keep going with our other bundles.

				if( err ) _this.emit( 'error', err );
				else if( bundleWasWritten ) _this.emit( 'bundleWritten', thisBundlePath, thisAssetType, true );

				nextEach();
			} );
		}, function( err ) {
			if( err ) _this.emit( 'error', err );

			 // done );
		} );
	} );
}
```
- example usage
```shell
...
				}, function( nextSeries ) {
					if( options.watch ) {
						// we only create glob watchers for the packages that parcel added to the manifest. Again, we want to avoid doubling up
						// work in situations where we have multiple parcelify instances running that share common bundles
						_.each( packagesThatWereCreated, function( thisPackage ) {
							thisPackage.createWatchers( assetTypes, browserifyInstance._options.packageFilter, options.appTransforms, options.appTransformDirs
 );
							if( thisPackage.isParcel ) {
								thisPackage.attachWatchListeners( options.bundlesByEntryPoint[ thisPackage.mainPath ] );
							}
						} );
					}

					if( ! _this.watching ) _this.emit( 'done' );

					nextSeries();
...
```

#### <a name="apidoc.element.parcelify.parcel.prototype.calcParcelAssets"></a>[function <span class="apidocSignatureSpan">parcelify.parcel.prototype.</span>calcParcelAssets ( assetTypes )](#apidoc.element.parcelify.parcel.prototype.calcParcelAssets)
- description and source-code
```javascript
calcParcelAssets = function ( assetTypes ) {
	memo = {};
	assetTypes.forEach( function( thisAssetType ) { memo[ thisAssetType ] = []; } );

	var sortedAssets = this.sortedDependencies.concat( this ).reduce( function( memo, thisPackage ) {
		var thisPackageAssets = thisPackage.assetsByType;

		_.each( thisPackageAssets, function( assets, thisAssetType ) {
			if( _.contains( assetTypes, thisAssetType ) )
				memo[ thisAssetType ] = memo[ thisAssetType ].concat( assets );
		} );

		return memo;
	}, memo );

	this.parcelAssetsByType = _.extend( {}, this.parcelAssetsByType, sortedAssets );
}
```
- example usage
```shell
...

					thisPackage = packagesThatWereCreated[ thisPackageId ] = new Parcel( packageOptions );
					thisPackage.createAllAssets( assetTypes );

					oldDependentParcels.forEach( function( thisDependentParcel ) {
						thisPackage.addDependentParcel( thisDependentParcel );
						thisDependentParcel.calcSortedDependencies();
						thisDependentParcel.calcParcelAssets( assetTypes );
					} );

					log.warn( '', 'Recreated package at ' + thisPackage.path + ' as Parcel.' );
				} else
					thisPackage = existingPacakages[ thisPackageId ];

				nextWaterfall();
...
```

#### <a name="apidoc.element.parcelify.parcel.prototype.calcSortedDependencies"></a>[function <span class="apidocSignatureSpan">parcelify.parcel.prototype.</span>calcSortedDependencies ()](#apidoc.element.parcelify.parcel.prototype.calcSortedDependencies)
- description and source-code
```javascript
calcSortedDependencies = function () {
	var packagesWithDependencies = [];

	function getEdgesForPackageDependencyGraph( thisPackage, thisTreeLevel, packageTreeLevels ) {
		if( _.isUndefined( thisTreeLevel ) ) thisTreeLevel = 0;
		if( _.isUndefined( packageTreeLevels ) ) packageTreeLevels = {};

		if( ! packageTreeLevels[ thisPackage.path ] ) packageTreeLevels[ thisPackage.path ] = thisTreeLevel;

		return thisPackage.dependencies.reduce( function( memo, thisDependentPackage ) {
			// these conditionals are to avoid cycles and infinite recursion.
			// first, we only traverse each node once to avoid infinite recursion.
			if( _.isUndefined( packageTreeLevels[ thisDependentPackage.path ] ) ) {
				memo = memo.concat( getEdgesForPackageDependencyGraph( thisDependentPackage, thisTreeLevel + 1, packageTreeLevels ) );
			}

			// second, we keep track of the levels of the nodes in the dependency tree (where
			// level 0 is the root node i.e. the parcel itself). nodes can only have dependencies
			// on other nodes with a level equal to or greater than their own. done.
			if( packageTreeLevels[ thisDependentPackage.path ] >= packageTreeLevels[ thisPackage.path ] ) {
				memo = memo.concat( [ [ thisPackage, thisDependentPackage ] ] );
			}

			return memo;
		}, [] );
	}

	var edges = getEdgesForPackageDependencyGraph( this );
	var sortedPackages = toposort( edges ).reverse();

	//sortedPackages = _.union( sortedPackages, Object.keys( packageManifest ) ); // union cuz some packages have no dependencies!
	sortedPackages = _.without( sortedPackages, this );

	this.sortedDependencies = sortedPackages;
}
```
- example usage
```shell
...
					oldPackage.destroy();

					thisPackage = packagesThatWereCreated[ thisPackageId ] = new Parcel( packageOptions );
					thisPackage.createAllAssets( assetTypes );

					oldDependentParcels.forEach( function( thisDependentParcel ) {
						thisPackage.addDependentParcel( thisDependentParcel );
						thisDependentParcel.calcSortedDependencies();
						thisDependentParcel.calcParcelAssets( assetTypes );
					} );

					log.warn( '', 'Recreated package at ' + thisPackage.path + ' as Parcel.' );
				} else
					thisPackage = existingPacakages[ thisPackageId ];
...
```

#### <a name="apidoc.element.parcelify.parcel.prototype.writeBundle"></a>[function <span class="apidocSignatureSpan">parcelify.parcel.prototype.</span>writeBundle ( assetType, dstPath, callback )](#apidoc.element.parcelify.parcel.prototype.writeBundle)
- description and source-code
```javascript
writeBundle = function ( assetType, dstPath, callback ) {
	var _this = this;
		
	var srcAssets = _this.parcelAssetsByType[ assetType ];
	if( ! srcAssets || srcAssets.length === 0 ) return callback( null, false ); // we don't want to create an empty bundle just because
 we have no source files

	var bundle = through2();
	var tempBundlePath = path.join( path.dirname( dstPath ), '.temp_' + path.basename( dstPath ) );

	bundle.pipe( fs.createWriteStream( dstPath ) ).on( 'close', function ( err ) {
		// execution resumes here after all the individual asset streams
		// have been piped to this bundle. we need to pipe the bundle to the writable
		// stream first (before individual assets are piped to bundle stream)
		// so that if the high water mark is reached on one of the readable streams
		// it doesn't pause (with no way to resume). See github issue #15.
		
		if( err ) return callback( err, false );

		// fs.rename( tempBundlePath, dstPath, function( err ) {
		// 	if( err ) console.log( 'yoyoyoo', fs.existsSync( tempBundlePath ), dstPath, srcAssets );

		// 	if( err ) return callback( err );

			//_this.bundlePathsByType[ assetType ] = dstPath; // don't do this. isn't really a property of the parcel so much as an input
 to parcelify

			callback( null, true );
		// } );
	} );

	// pipe all our individual style streams to the bundle in order to concatenate them
	async.eachSeries( srcAssets, function( thisAsset, nextAsset ) {
		var thisAssetStream = thisAsset.createReadStream();

		thisAssetStream.on( 'error', function( err ) {
			nextAsset( new Error( 'While reading or transforming "' + thisAsset.srcPath + '":\n' + err.message ) );
		} );

		thisAssetStream.on( 'end', function( err ) {
			nextAsset();
		} );

		thisAssetStream.pipe( bundle, { end : false } );
	}, function( err ) {
		if( err ) return callback( err, false );

		bundle.end();
		
		// execution will resume up above on the
		// 'close' event handler for our bundle
	} );
}
```
- example usage
```shell
...

						var thisParcelBundles = options.bundlesByEntryPoint[ thisParcel.mainPath ];
					
						async.each( Object.keys( thisParcelBundles ), function( thisAssetType, nextEach ) {
							var thisBundlePath = thisParcelBundles[ thisAssetType ];
							if( ! thisBundlePath ) return nextEach();

							thisParcel.writeBundle( thisAssetType, thisBundlePath, function( err, bundleWasWritten ) {
								// don't stop writing other bundles if there was an error on this one. errors happen
								// frequently with transforms.. like invalid scss, etc. don't stop the show, just
								// keep going with our other bundles.

								if( err ) _this.emit( 'error', err );
								else if( bundleWasWritten ) _this.emit( 'bundleWritten', thisBundlePath, thisAssetType, thisParcel, _this.watching );
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
