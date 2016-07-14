# THIS FILE IS GENERATED. Edit BUILD.pre, and then run build_tools/piplibgen.

package(default_visibility = ['//visibility:public'])

load('/build_tools/bazel/cc', 'prefer_pic_library')
load('/build_tools/bazel/py', 'dbx_py_local_piplib')

prefer_pic_library(
  name = 'protobuf',
  library = '//thirdparty/protobuf:protobuf',
)

prefer_pic_library(
  name = 'protobuf_lite',
  library = '//thirdparty/protobuf:protobuf_lite',
)

dbx_py_local_piplib(
  name = 'pyprotobuf',
  contents = ['google/protobuf/__init__.py', 'google/protobuf/any_pb2.py', 'google/protobuf/any_test_pb2.py', 'google/protobuf/api_pb2.py', 'google/protobuf/descriptor.py', 'google/protobuf/descriptor_database.py', 'google/protobuf/descriptor_pb2.py', 'google/protobuf/descriptor_pool.py', 'google/protobuf/duration_pb2.py', 'google/protobuf/empty_pb2.py', 'google/protobuf/field_mask_pb2.py', 'google/protobuf/json_format.py', 'google/protobuf/map_unittest_pb2.py', 'google/protobuf/message.py', 'google/protobuf/message_factory.py', 'google/protobuf/proto_builder.py', 'google/protobuf/reflection.py', 'google/protobuf/service.py', 'google/protobuf/service_reflection.py', 'google/protobuf/source_context_pb2.py', 'google/protobuf/struct_pb2.py', 'google/protobuf/symbol_database.py', 'google/protobuf/text_encoding.py', 'google/protobuf/text_format.py', 'google/protobuf/timestamp_pb2.py', 'google/protobuf/type_pb2.py', 'google/protobuf/unittest_arena_pb2.py', 'google/protobuf/unittest_custom_options_pb2.py', 'google/protobuf/unittest_import_pb2.py', 'google/protobuf/unittest_import_public_pb2.py', 'google/protobuf/unittest_mset_pb2.py', 'google/protobuf/unittest_mset_wire_format_pb2.py', 'google/protobuf/unittest_no_arena_import_pb2.py', 'google/protobuf/unittest_no_arena_pb2.py', 'google/protobuf/unittest_no_generic_services_pb2.py', 'google/protobuf/unittest_pb2.py', 'google/protobuf/unittest_proto3_arena_pb2.py', 'google/protobuf/wrappers_pb2.py', 'google/protobuf/internal/__init__.py', 'google/protobuf/internal/_api_implementation.so', 'google/protobuf/internal/_parameterized.py', 'google/protobuf/internal/any_test_pb2.py', 'google/protobuf/internal/api_implementation.py', 'google/protobuf/internal/containers.py', 'google/protobuf/internal/decoder.py', 'google/protobuf/internal/descriptor_database_test.py', 'google/protobuf/internal/descriptor_pool_test.py', 'google/protobuf/internal/descriptor_pool_test1_pb2.py', 'google/protobuf/internal/descriptor_pool_test2_pb2.py', 'google/protobuf/internal/descriptor_test.py', 'google/protobuf/internal/encoder.py', 'google/protobuf/internal/enum_type_wrapper.py', 'google/protobuf/internal/factory_test1_pb2.py', 'google/protobuf/internal/factory_test2_pb2.py', 'google/protobuf/internal/file_options_test_pb2.py', 'google/protobuf/internal/generator_test.py', 'google/protobuf/internal/json_format_test.py', 'google/protobuf/internal/message_factory_test.py', 'google/protobuf/internal/message_listener.py', 'google/protobuf/internal/message_set_extensions_pb2.py', 'google/protobuf/internal/message_test.py', 'google/protobuf/internal/missing_enum_values_pb2.py', 'google/protobuf/internal/more_extensions_dynamic_pb2.py', 'google/protobuf/internal/more_extensions_pb2.py', 'google/protobuf/internal/more_messages_pb2.py', 'google/protobuf/internal/packed_field_test_pb2.py', 'google/protobuf/internal/proto_builder_test.py', 'google/protobuf/internal/python_message.py', 'google/protobuf/internal/reflection_test.py', 'google/protobuf/internal/service_reflection_test.py', 'google/protobuf/internal/symbol_database_test.py', 'google/protobuf/internal/test_bad_identifiers_pb2.py', 'google/protobuf/internal/test_util.py', 'google/protobuf/internal/text_encoding_test.py', 'google/protobuf/internal/text_format_test.py', 'google/protobuf/internal/type_checkers.py', 'google/protobuf/internal/unknown_fields_test.py', 'google/protobuf/internal/well_known_types.py', 'google/protobuf/internal/well_known_types_test.py', 'google/protobuf/internal/wire_format.py', 'google/protobuf/internal/wire_format_test.py', 'google/protobuf/internal/import_test_package/__init__.py', 'google/protobuf/internal/import_test_package/inner_pb2.py', 'google/protobuf/internal/import_test_package/outer_pb2.py', 'google/protobuf/pyext/__init__.py', 'google/protobuf/pyext/_message.so', 'google/protobuf/pyext/cpp_message.py', 'google/protobuf/pyext/python_pb2.py', 'protobuf-3.0.0b3-py2.7.egg-info/PKG-INFO', 'protobuf-3.0.0b3-py2.7.egg-info/SOURCES.txt', 'protobuf-3.0.0b3-py2.7.egg-info/dependency_links.txt', 'protobuf-3.0.0b3-py2.7.egg-info/namespace_packages.txt', 'protobuf-3.0.0b3-py2.7.egg-info/requires.txt', 'protobuf-3.0.0b3-py2.7.egg-info/top_level.txt', 'google/__init__.py'],
  srcs = glob(['**/*.*']),
  global_options = [
    '--cpp_implementation',
    '--link-libprotobuf-static=$(ROOT)/$(location :protobuf)',
    '--link-libprotobuf-static=$(ROOT)/$(location :protobuf_lite)',
    # setup.py tries to make sure ../src is on the include path. This doesn't work because pip
    # builds the extension outside of the tree, so we manually add the right include path.
    'build_ext', '--include-dirs=$(ROOT)/thirdparty/protobuf/src',
  ],
  deps = [
    ':protobuf',
    ':protobuf_lite',
    '//thirdparty/protobuf:protoc',
    '//pip/six',
  ],
  env = {
    'PROTROOT': '$(ROOT)/thirdparty/protobuf/src/',
    'PROTOC': '$(ROOT)/$(location //thirdparty/protobuf:protoc)',
  },
  provides = ['google.protobuf', 'google.protobuf.descriptor'],
)
