#### 0.1.13 (2024-06-08)

##### Chores

* **deps:**
  *  update dependency react-pdf to v8 ([f54d0585](https://github.com/summit-electric-supply/react-doc-viewer/commit/f54d05855f764ca1c522157116e832ee8ca7caf0))
  *  update dependency pdfjs-dist to v4 ([556a0956](https://github.com/summit-electric-supply/react-doc-viewer/commit/556a0956c4447bdf95a8bf17ea5595cf97c54fdd))
*  Added default height to loading container ([e5570741](https://github.com/summit-electric-supply/react-doc-viewer/commit/e55707411ec025e60914fcbe49ae6ffcb0204194))
*  Removed unused css file ([485f15b3](https://github.com/summit-electric-supply/react-doc-viewer/commit/485f15b3def21723af8b422cf4a0d71fe1aeb109))
*  No longer require public folder ([2a639dcc](https://github.com/summit-electric-supply/react-doc-viewer/commit/2a639dcc2ff0ad22ea1fb65caed40ca700ff0bdd))
*  Renamed MainContext to DocViewerContext for external plugins to import it with a less generic name ([c433d438](https://github.com/summit-electric-supply/react-doc-viewer/commit/c433d438455f8887a3f972fab2ca8de7203eb000))
*  Removed old pdf plugin dependencies ([3baa9355](https://github.com/summit-electric-supply/react-doc-viewer/commit/3baa9355516b9ea70eb0c3cd449bf40d52d12fd0))

##### Documentation Changes

*  README - styled component example is missing a closing bracket after DocViewer Fixes [#31](https://github.com/summit-electric-supply/react-doc-viewer/pull/31) ([7964c0b9](https://github.com/summit-electric-supply/react-doc-viewer/commit/7964c0b931b3ec27e3adc5c0d5c7382644e0407c))
*  README - styled component example is missing a closing bracket after DocViewer Fixes [#31](https://github.com/summit-electric-supply/react-doc-viewer/pull/31) ([da0a40ee](https://github.com/summit-electric-supply/react-doc-viewer/commit/da0a40ee09a76c175cb5ec67de3577f31e19ae4a))
*  README updated ([819acb5b](https://github.com/summit-electric-supply/react-doc-viewer/commit/819acb5ba23167b29b896bd6808123dd9cc45191))
*  Removed Setup Demo from contents at top of README ([8a8db314](https://github.com/summit-electric-supply/react-doc-viewer/commit/8a8db31450ec8d9391c7599eba517c2754bc7467))
*  Added README info for importing and using the included individual renderers ([3a87cf87](https://github.com/summit-electric-supply/react-doc-viewer/commit/3a87cf87b1a259b106790d3676cfa6a1854a575e))
*  README updated ([39fd2b93](https://github.com/summit-electric-supply/react-doc-viewer/commit/39fd2b931ab1255260be91adb1a8b79433946904))

##### New Features

* **TIF:**  Added .tif as an option to render within TIFFRenderer. ([a32f9b0f](https://github.com/summit-electric-supply/react-doc-viewer/commit/a32f9b0ffff1a0a37d14a6dd948e1d0f52ffe6c6))
* **FileName Header:**
  *  decodeURI when rendering fileName in header title ([79c0da83](https://github.com/summit-electric-supply/react-doc-viewer/commit/79c0da83fecee0b4ae3af174f12068a8472dc377))
  *  When rendering fileName in header, remove url params unless requested to keep ([109da8d7](https://github.com/summit-electric-supply/react-doc-viewer/commit/109da8d7847fe8d6338f2c303491e12ae97506cf))
* **Combine File Loaders:**  File Loaders duplicate code combined, also base64 and arrayBuffer combined into fileData ([#47](https://github.com/summit-electric-supply/react-doc-viewer/pull/47)) ([f3fd9952](https://github.com/summit-electric-supply/react-doc-viewer/commit/f3fd9952ad27012dc619860ac180bb6abe5cdf8f))
*  BMP Image renderer added ([2cb03e4c](https://github.com/summit-electric-supply/react-doc-viewer/commit/2cb03e4c8dbdae1f7c2090c45dc4d9f71d70f571))
*  Internal ImageProxyRenderer created, that can be used by all other Image renderers, and styled by them ([90e575da](https://github.com/summit-electric-supply/react-doc-viewer/commit/90e575dac21e4656601a593817c9f74280352c42))
*  BMP Image renderer added ([2e8578b1](https://github.com/summit-electric-supply/react-doc-viewer/commit/2e8578b127f61e855cab9371fb32f193eea88742))
*  Internal ImageProxyRenderer created, that can be used by all other Image renderers, and styled by them ([dc2afb71](https://github.com/summit-electric-supply/react-doc-viewer/commit/dc2afb71f58edd9ae719b1fd08218193df469120))
*  Added renderer for .msg file extension ([b4cf7bf4](https://github.com/summit-electric-supply/react-doc-viewer/commit/b4cf7bf4d78cef18d06435bb2a96902fcc210c77))
*  useDocumentLoader hook now allows use of custom fileLoaders. e.g. bse64, ArrayBuffer ([ebc9a454](https://github.com/summit-electric-supply/react-doc-viewer/commit/ebc9a45451945f7ee0502bf2046f6d0be82aff38))
*  pluginRenderers are now passed directly to the main state context, and the correct renderer is retrieved from there depending on it's fileType associations ([4c7abfd3](https://github.com/summit-electric-supply/react-doc-viewer/commit/4c7abfd3fa7f83289d1118ab4f6744006ee28ec6))
*  Removed FontAwesome and included replacement svgs, which are resizable and colourable ([7c7c3fca](https://github.com/summit-electric-supply/react-doc-viewer/commit/7c7c3fca7e7ec36040369eba5a0c010031cd225a))
*  implemented ability to fully replace the contents of the header, but also retain access to the state and document navigation actions ([2c1e3d0d](https://github.com/summit-electric-supply/react-doc-viewer/commit/2c1e3d0db453fb0deb8c3ea944f94cbf10840462))
* **Merge Default Plugins:**  Plugins have been pulled back into the component package, Updated README to inform on updated and better way to use included and custom plugins ([34bed0c7](https://github.com/summit-electric-supply/react-doc-viewer/commit/34bed0c7e1c33a7f1bc6eb4b5895945913a49586))

##### Bug Fixes

* **TIFFRenderer file Corrupt:**  Don't crash if parseTIFF fails because of corrupted file. ([30755e57](https://github.com/summit-electric-supply/react-doc-viewer/commit/30755e57ec0bef8a665ce1c6f9e8f93c4ada55dc))
* **TIFFRenderer crash:**  If parseTiff is supplied with an undefined tiffArrayBuffer. Return out. ([eedeac1e](https://github.com/summit-electric-supply/react-doc-viewer/commit/eedeac1e0deada4126e77058d5c52b1ed92f200f))
*  Added github url to npm package ([b713957f](https://github.com/summit-electric-supply/react-doc-viewer/commit/b713957fef42e896ab45d99a3127a59e98a11e60))
*  Document fetches header even if file type is supplied ([b5296d0f](https://github.com/summit-electric-supply/react-doc-viewer/commit/b5296d0f38a72e59407c5f1d4a34b10d9e7f439e))
*  Changed Button to actual <button> from <a> to prevent annoying text selection bug ([25dc93eb](https://github.com/summit-electric-supply/react-doc-viewer/commit/25dc93ebf2dfc31a59619ff4ab2350a72d774471))
*  Abort fetch of file when new file is selected mid fetch. Also display loading spinner ([db440e66](https://github.com/summit-electric-supply/react-doc-viewer/commit/db440e664e3ec7455b94a0d17bda7804d944396d))
*  IIconProps import type fixed ([1e1b00c5](https://github.com/summit-electric-supply/react-doc-viewer/commit/1e1b00c5b5ed7a7a9b7261d12875cb2cfc5bd744))
*  Removed necessity for 2 context calls ([1e9886ca](https://github.com/summit-electric-supply/react-doc-viewer/commit/1e9886cae3fe48cf217e47eee90f323aac9474b3))
*  Pass mainState context to CurrentRenderer for ease of use/access to loaded data, and other mainState props ([98efa91c](https://github.com/summit-electric-supply/react-doc-viewer/commit/98efa91ce7c157898658260a8b51e940ca4a905d))
*  If user passes in a bad file / url and uri ends up not being useful, ([ae99034f](https://github.com/summit-electric-supply/react-doc-viewer/commit/ae99034f0ab63c1e13aca054d43177df9fc7aff8))
*  FileType removed, as the component needs to be ambiguous to plugin renderers ([fcf9e1c0](https://github.com/summit-electric-supply/react-doc-viewer/commit/fcf9e1c01eba523a6746c42f85f88704159eca91))

##### Other Changes

* fix/pptx ([60c27812](https://github.com/summit-electric-supply/react-doc-viewer/commit/60c27812f658d4edf4a7cc1673c26a95b838eca1))
* Alcumus/react-doc-viewer into develop ([2184d46c](https://github.com/summit-electric-supply/react-doc-viewer/commit/2184d46c53792eee468995b041dbc9b28fdd0e07))
* mattmogford-alcumus/40_Create-HTMLRenderer ([9eff64e2](https://github.com/summit-electric-supply/react-doc-viewer/commit/9eff64e20d2278c3b76234a6b24f4464e7c0acb7))
* mattmogford-alcumus/issue29 ([35ea44eb](https://github.com/summit-electric-supply/react-doc-viewer/commit/35ea44eb103e5bd1ce43e4bd6c63e3b12f956f22))
* develop ([66cd5676](https://github.com/summit-electric-supply/react-doc-viewer/commit/66cd5676b5dde2efe49beae7a56c78c4b42cbc98))
* mattmogford-alcumus/issue19 ([f8f16bc1](https://github.com/summit-electric-supply/react-doc-viewer/commit/f8f16bc166d1f4d5e7682f3ace63d6515a8fe2ee))

##### Refactors

*  Reverting from Recoil to react state, context and reducers ([ff26a49b](https://github.com/summit-electric-supply/react-doc-viewer/commit/ff26a49be58e6c4f01db033ec82fb8b934373b83))

##### Tests

*  Updated test snapshot ([7660907f](https://github.com/summit-electric-supply/react-doc-viewer/commit/7660907f604ad70433d2cc0fc219a895e1c26787))
*  Updated snapshots for tests ([f40a5447](https://github.com/summit-electric-supply/react-doc-viewer/commit/f40a54478d773949c0ebde4b9e2d64eec1133c74))

#### 0.1.11 (2024-05-14)

#### 0.1.10 (2024-05-14)

#### 0.1.9 (2024-05-14)

#### 0.1.8 (2024-05-14)

##### Chores

* **deps:**  update dependency react-pdf to v8 ([f54d0585](https://github.com/Alcumus/react-doc-viewer/commit/f54d05855f764ca1c522157116e832ee8ca7caf0))

#### 0.1.7 (2024-05-13)

##### Chores

* **deps:**  update dependency pdfjs-dist to v4 ([556a0956](https://github.com/Alcumus/react-doc-viewer/commit/556a0956c4447bdf95a8bf17ea5595cf97c54fdd))

#### 0.1.6 (2024-05-13)

#### 0.1.5 (2020-10-29)

##### Bug Fixes

* **TIFFRenderer file Corrupt:**  Don't crash if parseTIFF fails because of corrupted file. ([30755e57](https://github.com/Alcumus/react-doc-viewer/commit/30755e57ec0bef8a665ce1c6f9e8f93c4ada55dc))

#### 0.1.4 (2020-10-29)

##### Bug Fixes

* **TIFFRenderer crash:**  If parseTiff is supplied with an undefined tiffArrayBuffer. Return out. ([eedeac1e](https://github.com/Alcumus/react-doc-viewer/commit/eedeac1e0deada4126e77058d5c52b1ed92f200f))

#### 0.1.3 (2020-10-29)

##### New Features

* **TIF:**  Added .tif as an option to render within TIFFRenderer. ([a32f9b0f](https://github.com/Alcumus/react-doc-viewer/commit/a32f9b0ffff1a0a37d14a6dd948e1d0f52ffe6c6))

##### Other Changes

* fix/pptx ([60c27812](https://github.com/Alcumus/react-doc-viewer/commit/60c27812f658d4edf4a7cc1673c26a95b838eca1))

#### 0.1.2 (2020-10-26)

##### Bug Fixes

*  Added github url to npm package ([b713957f](https://github.com/Alcumus/react-doc-viewer/commit/b713957fef42e896ab45d99a3127a59e98a11e60))

#### 0.1.1 (2020-10-26)

##### New Features

* **FileName Header:**
  *  decodeURI when rendering fileName in header title (79c0da83)
  *  When rendering fileName in header, remove url params unless requested to keep (109da8d7)

#### 0.0.43 (2020-09-30)

##### New Features

* **Combine File Loaders:**  File Loaders duplicate code combined, also base64 and arrayBuffer combined into fileData (#47) (f3fd9952)

#### 0.0.42 (2020-09-30)

##### Documentation Changes

*  README - styled component example is missing a closing bracket after DocViewer Fixes #31 (da0a40ee)

##### New Features

*  BMP Image renderer added (2e8578b1)
*  Internal ImageProxyRenderer created, that can be used by all other Image renderers, and styled by them (dc2afb71)

##### Other Changes

* Alcumus/react-doc-viewer into develop (2184d46c)
* mattmogford-alcumus/40_Create-HTMLRenderer (9eff64e2)

#### 0.0.41 (2020-09-25)

#### 0.0.40 (2020-09-24)

##### Documentation Changes

*  README - styled component example is missing a closing bracket after DocViewer Fixes #31 (7964c0b9)

##### New Features

*  BMP Image renderer added (2cb03e4c)
*  Internal ImageProxyRenderer created, that can be used by all other Image renderers, and styled by them (90e575da)

#### 0.0.39 (2020-09-23)

##### Documentation Changes

*  README updated (819acb5b)

#### 0.0.38 (2020-09-23)

##### New Features

*  Added renderer for .msg file extension (b4cf7bf4)
*  useDocumentLoader hook now allows use of custom fileLoaders. e.g. bse64, ArrayBuffer (ebc9a454)

#### 0.0.37 (2020-09-18)

##### Other Changes

* mattmogford-alcumus/issue29 (35ea44eb)

#### 0.0.36 (2020-09-17)

#### 0.0.35 (2020-09-17)

#### 0.0.34 (2020-09-16)

##### Bug Fixes

*  Document fetches header even if file type is supplied (b5296d0f)

#### 0.0.33 (2020-09-16)

##### Other Changes

* develop (66cd5676)
* mattmogford-alcumus/issue19 (f8f16bc1)

#### 0.0.32 (2020-09-03)

##### Chores

*  Added default height to loading container (e5570741)

##### New Features

*  pluginRenderers are now passed directly to the main state context, and the correct renderer is retrieved from there depending on it's fileType associations (4c7abfd3)

##### Bug Fixes

*  Changed Button to actual <button> from <a> to prevent annoying text selection bug (25dc93eb)
*  Abort fetch of file when new file is selected mid fetch. Also display loading spinner (db440e66)

##### Tests

*  Updated test snapshot (7660907f)

#### 0.0.31 (2020-09-02)

##### Chores

*  Removed unused css file (485f15b3)

##### New Features

*  Removed FontAwesome and included replacement svgs, which are resizable and colourable (7c7c3fca)

##### Bug Fixes

*  IIconProps import type fixed (1e1b00c5)

##### Tests

*  Updated snapshots for tests (f40a5447)

#### 0.0.30 (2020-09-02)

##### New Features

*  implemented ability to fully replace the contents of the header, but also retain access to the state and document navigation actions (2c1e3d0d)

#### 0.0.29 (2020-09-01)

##### Chores

*  No longer require public folder (2a639dcc)

#### 0.0.28 (2020-09-01)

##### Bug Fixes

*  Removed necessity for 2 context calls (1e9886ca)

#### 0.0.27 (2020-09-01)

##### Documentation Changes

*  Removed Setup Demo from contents at top of README (8a8db314)

#### 0.0.26 (2020-09-01)

##### Bug Fixes

*  Pass mainState context to CurrentRenderer for ease of use/access to loaded data, and other mainState props (98efa91c)

#### 0.0.25 (2020-09-01)

##### Chores

*  Renamed MainContext to DocViewerContext for external plugins to import it with a less generic name (c433d438)

##### Documentation Changes

*  Added README info for importing and using the included individual renderers (3a87cf87)

##### Refactors

*  Reverting from Recoil to react state, context and reducers (ff26a49b)

#### 0.0.24 (2020-08-28)

#### 0.0.23 (2020-08-28)

#### 0.0.22 (2020-08-28)

##### New Features

* **Merge Default Plugins:**  Plugins have been pulled back into the component package, Updated README to inform on updated and better way to use included and custom plugins (34bed0c7)

##### Bug Fixes

*  If user passes in a bad file / url and uri ends up not being useful, (ae99034f)

#### 0.0.21 (2020-08-27)

##### Chores

*  Removed old pdf plugin dependencies (3baa9355)

#### 0.0.20 (2020-08-27)

#### 0.0.19 (2020-08-26)

##### Documentation Changes

*  README updated (39fd2b93)

##### Bug Fixes

*  FileType removed, as the component needs to be ambiguous to plugin renderers (fcf9e1c0)

#### 0.0.18 (2020-08-26)

#### 0.0.17 (2020-08-25)

#### 0.0.16 (2020-08-25)

#### 0.0.15 (2020-08-25)

#### 0.0.14 (2020-08-25)

#### 0.0.13 (2020-08-25)

#### 0.0.12 (2020-08-25)

##### Chores

*  Tidied state atoms etc. (fbb5ede2)

##### Bug Fixes

* **PDFRenderer Reset Zoom Broken:**  resetZoomLevel function wasn't being called (4b3b9918)

#### 0.0.12 (2020-08-25)

##### Bug Fixes

* **PDFRenderer Reset Zoom Broken:**  resetZoomLevel function wasn't being called (4b3b9918)

#### 0.0.11 (2020-08-25)

##### Bug Fixes

*  sever was incorrect for build-release options (2ebe713b)

##### Tests

*  Added example png for testing purposes (9c3c6cf6)

#### 0.0.10 (2020-08-24)

#### 0.0.9 (2020-08-24)

#### 0.0.8 (2020-08-24)

##### Bug Fixes

*  ignore index on building package, point main and types to main component file DocViewer.tsx (96f1a12f)

#### 0.0.4 (2020-08-24)

##### New Features

* **Versioning:**  Added scripts for auto update CHANGELOG with versioning (31c31d1c)

##### Bug Fixes

*  config is optional and so could be undefined (596d611d)

#### 0.0.3 (2020-08-24)

##### New Features

- **Versioning:** Added scripts for auto update CHANGELOG with versioning (48536a0c)

##### Bug Fixes

- config is optional and so could be undefined (596d611d)

#### 0.0.3 (2020-08-24)

##### Bug Fixes

- config is optional and so could be undefined (596d611d)
