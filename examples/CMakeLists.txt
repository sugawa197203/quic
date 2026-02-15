set(base_examples
    quic-pacing
    quic-tester
    quic-tester-streams
    quic-variants-comparison-bulksend
    quic-variants-comparison
)

foreach(example IN LISTS base_examples)
  build_lib_example(
    NAME ${example}
    SOURCE_FILES ${example}.cc
    LIBRARIES_TO_LINK
      ${libcore}
      ${libquic}
    LIBRARIES_TO_LINK
      ${libcore}
      ${libquic}
      ${libinternet}
      ${libapplications}
      ${libflow-monitor}
      ${libpoint-to-point}
  )
endforeach()
