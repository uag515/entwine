set(MODULE types)
set(BASE "${CMAKE_CURRENT_SOURCE_DIR}")

set(
    SOURCES
    "${BASE}/bounds.cpp"
    "${BASE}/format.cpp"
    "${BASE}/format-packing.cpp"
    "${BASE}/metadata.cpp"
    "${BASE}/pooled-point-table.cpp"
    "${BASE}/structure.cpp"
    "${BASE}/subset.cpp"
    "${BASE}/tube.cpp"
)

set(
    HEADERS
    "${BASE}/bounds.hpp"
    "${BASE}/defs.hpp"
    "${BASE}/dim-info.hpp"
    "${BASE}/dir.hpp"
    "${BASE}/fixed-point-layout.hpp"
    "${BASE}/format.hpp"
    "${BASE}/format-packing.hpp"
    "${BASE}/format-types.hpp"
    "${BASE}/metadata.hpp"
    "${BASE}/outer-scope.hpp"
    "${BASE}/point.hpp"
    "${BASE}/point-pool.hpp"
    "${BASE}/pooled-point-table.hpp"
    "${BASE}/reprojection.hpp"
    "${BASE}/schema.hpp"
    "${BASE}/structure.hpp"
    "${BASE}/subset.hpp"
    "${BASE}/tube.hpp"
    "${BASE}/vector-point-table.hpp"
)

install(FILES ${HEADERS} DESTINATION include/entwine/${MODULE})
add_library(${MODULE} OBJECT ${SOURCES})

