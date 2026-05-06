file(GLOB LIQUID_CPP_SRC liquid_cpp/src/*.cpp)

idf_component_register(
        SRCS ${LIQUID_CPP_SRC}
        INCLUDE_DIRS "rapidjson/include" "liquid_cpp/src"
)

target_compile_definitions(${COMPONENT_LIB} PRIVATE LIQUID_INCLUDE_RAPIDJSON_VARIABLE=1)
