IF (HAVE_STL)
    PLAYERDRIVER_OPTION (erratic build_erratic ON)
ELSE (HAVE_STL)
    PLAYERDRIVER_OPTION (erratic build_erratic OFF "STL not found.")
ENDIF (HAVE_STL)
PLAYERDRIVER_REJECT_OS (erratic build_erratic PLAYER_OS_WIN)
PLAYERDRIVER_ADD_DRIVER (erratic build_erratic SOURCES erratic.cc motorpacket.cc packet.cc robot_params.cc sip.cc)
