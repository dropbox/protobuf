package(default_visibility = ['//visibility:public'])

filegroup(
  name = '_setup',
  srcs = ['setup.py'],
)

genrule(
  name = '_pyprotobuf',
  srcs = glob(['**/*.cc', 'src/**/*.h', '**/*.py', '**/*.proto']) + [':_setup', '//thirdparty/protobuf:protoc', '//thirdparty/protobuf:protobuf'],
  outs = [
    'pyprotobuf.pip.zip',
    ],
  cmd = 'export PROTOC=`readlink -f $(location //thirdparty/protobuf:protoc)`; ' +
  'out=`readlink -f $(@)`; out_dir=`readlink -f $(@D)`; ' +
  'libprotobuf=$$(readlink -f $$(dirname $(location //thirdparty/protobuf:protoc)))/libprotobuf.a; ' +
  'libprotobuf_lite=$$(readlink -f $$(dirname $(location //thirdparty/protobuf:protoc)))/libprotobuf_lite.a; ' +
  'cd `dirname $(location :_setup)`; ' +
  'PATH=/usr/bin:/bin /usr/local/bin/python ./setup.py --cpp_implementation --link-libprotobuf-static=$$libprotobuf --link-libprotobuf-static=$$libprotobuf_lite build --build-lib $$out_dir --build-temp $$out_dir-tmp && ' +
  'cd $$out_dir && /usr/bin/zip -qr $$out google',
)

py_library(
  name = 'pyprotobuf',
  data = [
    ':_pyprotobuf',
    '//pip:six',
  ],
)
