

#---------------------------------------------
# Adding the languages directories
#---------------------------------------------

# over view only projects
foreach (f ${OSGeoLiveDoc_OVERVIEW})
    if (OSGeoLiveDoc_VERBOSE_DEBUG)
        message(STATUS "        Adding overview ${f}")
    endif()
    configure_file("${f}_overview.rst" "${f}_overview.rst")
endforeach()

set(LOCAL
    "toc.rst"
    #"overview.rst"
    )

foreach (f ${LOCAL} )
    if (OSGeoLiveDoc_VERBOSE_DEBUG)
        message(STATUS "        Adding file ${f}")
    endif()
    configure_file("${f}" "${f}")
endforeach()

