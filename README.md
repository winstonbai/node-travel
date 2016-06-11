# **nodejs-travel nodejs旅行**#

Starting with 0,I'd like to go on a trip to nodejs. 从零开始,我想来一次说走就走的nodejs旅行

## 1.plain   计划

    三个月内,可构建高性能网站(开始时间20160610)
    
>## 2.preparation  准备

### 2.1.技能

    了解javascript基础,ES5,ES6基础,babel,CommonJS
    
### 2.2.环境

####操作系统
    whilewon@ubuntu:~/nodejs$ cat /proc/version
    Linux version 3.13.0-88-generic (buildd@lgw01-16) (gcc version 4.8.4 (Ubuntu 4.8.4-2ubuntu1~14.04.3) ) #135-Ubuntu SMP Wed Jun 8 21:10:42 UTC 2016
    
####nodejs依赖环境
    python2.7 ,python是一种开发语言,nodejs的项目构建工具GYP是基于python2.7开发的.
    GCC+  nodejs自身的部分是用c++写的，于是需要GCC+进行编译.
    
####安装nodejs

从源码编译,到安装，版本为4.4.5

    官方下载地址：https://nodejs.org/en/download/
    
    下载nodejs源码：https://nodejs.org/dist/v4.4.5/node-v4.4.5.tar.gz
    
    whilewon@ubuntu:~$ cd Downloads/
    
    whilewon@ubuntu:~/Downloads$ tar zxvf node-v4.4.5.tar.gz 
    
    whilewon@ubuntu:~/Downloads$ cd node-v4.4.5/   
      
    whilewon@ubuntu:~/Downloads/node-v4.4.5$ ./configure
    creating  ./icu_config.gypi
    { 'target_defaults': { 'cflags': [],
                           'default_configuration': 'Release',
                           'defines': [],
                           'include_dirs': [],
                           'libraries': []},
      'variables': { 'asan': 0,
                     'gas_version': 0,
                     'host_arch': 'x64',
                     'icu_small': 'false',
                     'node_byteorder': 'little',
                     'node_install_npm': 'true',
                     'node_prefix': '/usr/local',
                     'node_release_urlbase': '',
                     'node_shared_http_parser': 'false',
                     'node_shared_libuv': 'false',
                     'node_shared_openssl': 'false',
                     'node_shared_zlib': 'false',
                     'node_tag': '',
                     'node_use_dtrace': 'false',
                     'node_use_etw': 'false',
                     'node_use_lttng': 'false',
                     'node_use_openssl': 'true',
                     'node_use_perfctr': 'false',
                     'openssl_fips': '',
                     'openssl_no_asm': 0,
                     'target_arch': 'x64',
                     'uv_parent_path': '/deps/uv/',
                     'uv_use_dtrace': 'false',
                     'v8_enable_gdbjit': 0,
                     'v8_enable_i18n_support': 0,
                     'v8_no_strict_aliasing': 1,
                     'v8_optimized_debug': 0,
                     'v8_random_seed': 0,
                     'v8_use_snapshot': 'true',
                     'want_separate_host_toolset': 0}}
    creating  ./config.gypi
    creating  ./config.mk

    whilewon@ubuntu:~/Downloads/node-v4.4.5$ make
    
    whilewon@ubuntu:~/Downloads/node-v4.4.5$ sudo make install
    
    whilewon@ubuntu:~/Downloads/node-v4.4.5$ node -v
    v4.4.5
    
    whilewon@ubuntu:~/Downloads/node-v4.4.5$ npm -v
    2.15.5
    
    whilewon@ubuntu:/usr/local/bin$ which node
    /usr/local/bin/node


####2.3.工具

#####2.3.1.开发工具
    
    下载WebStorm-2016.1.3 (1).tar.gz
    
    解压：tar zxvf WebStorm-2016.1.3 (1).tar.gz
    
    cd work/WebStorm-145.1616.9/bin/
    
    sudo chmod 755 webstorm.sh
    
    ./webstorm.sh
    
#####2.3.2.debut工具
    whilewon@ubuntu:~$ sudo npm install -g node-inspector
     
    > v8-debug@0.7.7 preinstall /usr/local/lib/node_modules/node-inspector/node_modules/v8-debug
    > node -e 'process.exit(0)'
    
     
    > v8-profiler@5.6.5 preinstall /usr/local/lib/node_modules/node-inspector/node_modules/v8-profiler
    > node -e 'process.exit(0)'
    
     
    > v8-profiler@5.6.5 install /usr/local/lib/node_modules/node-inspector/node_modules/v8-profiler
    > node-pre-gyp install --fallback-to-build
    
    [v8-profiler] Success: "/usr/local/lib/node_modules/node-inspector/node_modules/v8-profiler/build/profiler/v5.6.5/node-v46-linux-x64/profiler.node" already installed
    Pass --update-binary to reinstall or --build-from-source to recompile
     
    > v8-debug@0.7.7 install /usr/local/lib/node_modules/node-inspector/node_modules/v8-debug
    > node-pre-gyp install --fallback-to-build
    
    [v8-debug] Success: "/usr/local/lib/node_modules/node-inspector/node_modules/v8-debug/build/debug/v0.7.7/node-v46-linux-x64/debug.node" is installed via remote
    /usr/local/bin/node-inspector -> /usr/local/lib/node_modules/node-inspector/bin/inspector.js
    /usr/local/bin/node-debug -> /usr/local/lib/node_modules/node-inspector/bin/node-debug.js
    node-inspector@0.12.8 /usr/local/lib/node_modules/node-inspector
    ├── path-is-absolute@1.0.0
    ├── async@0.9.2
    ├── semver@4.3.6
    ├── debug@2.2.0 (ms@0.7.1)
    ├── which@1.2.10 (isexe@1.1.2)
    ├── serve-favicon@2.3.0 (parseurl@1.3.1, etag@1.7.0, fresh@0.3.0, ms@0.7.1)
    ├── ws@1.1.0 (options@0.0.6, ultron@1.0.2)
    ├── strong-data-uri@1.0.4 (truncate@1.0.5)
    ├── rc@1.1.6 (ini@1.3.4, deep-extend@0.4.1, strip-json-comments@1.0.4, minimist@1.2.0)
    ├── glob@5.0.15 (inherits@2.0.1, once@1.3.3, inflight@1.0.5, minimatch@3.0.0)
    ├── yargs@3.32.0 (camelcase@2.1.1, decamelize@1.2.0, y18n@3.2.1, window-size@0.1.4, cliui@3.2.0, os-locale@1.4.0, string-width@1.0.1)
    ├── express@4.13.4 (escape-html@1.0.3, content-type@1.0.2, fresh@0.3.0, parseurl@1.3.1, array-flatten@1.1.1, cookie-signature@1.0.6, utils-merge@1.0.0, methods@1.1.2, merge-descriptors@1.0.1, vary@1.0.1, etag@1.7.0, cookie@0.1.5, path-to-regexp@0.1.7, range-parser@1.0.3, content-disposition@0.5.1, depd@1.1.0, qs@4.0.0, on-finished@2.3.0, finalhandler@0.4.1, proxy-addr@1.0.10, send@0.13.1, type-is@1.6.13, accepts@1.2.13, serve-static@1.10.3)
    ├── v8-profiler@5.6.5 (nan@2.3.5, node-pre-gyp@0.6.28)
    ├── biased-opener@0.2.8 (minimist@1.2.0, x-default-browser@0.3.1, browser-launcher2@0.4.6)
    └── v8-debug@0.7.7 (nan@2.3.5, node-pre-gyp@0.6.28)

#####2.3.3.部署工具
    
#####2.3.4.构建工具
    sudo npm install jade -g
    在Setting -->Tools-->File Watcher中增加，选择jade，
    sudo npm install -g babel
    在Setting -->Tools-->File Watcher中增加，选择babel，
    在保存 自定义的js文件时，控制台提示：
    /usr/local/bin/babel --source-maps --out-file app-compiled.js /home/whilewon/WebstormProjects/node-travel/app.js
    You have mistakenly installed the `babel` package, which is a no-op in Babel 6.
    Babel's CLI commands have been moved from the `babel` package to the `babel-cli` package.
    
        npm uninstall babel
        npm install babel-cli
    
    See http://babeljs.io/docs/usage/cli/ for setup instructions.
    错误的执行命令：
    whilewon@ubuntu:~$ npm uninstall babel
    npm WARN uninstall not installed in /home/whilewon/node_modules: "babel"
    因为当初安装时，就是-g，所以卸载时也应该是:
    sudo npm uninstall -g babel
     
    安装babel-cli
    sudo npm install -g babel-cli

>## 3.beginning  开始

###原理
    
###基础

###核心

###网站搭建
    
    创建一个工程：node-travel
    使用webstorm 创建nodejs express app工程
>## 4.summary  总结

###实际耗时

###心得体会
