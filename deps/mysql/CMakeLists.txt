# Copyright (C) 2008-2019 TrinityCore <https://www.trinitycore.org/>
# Copyright (C) 2016+     AzerothCore <www.azerothcore.org>, released under GNU AGPL3 v3 license: https://github.com/azerothcore/azerothcore-wotlk/blob/master/LICENSE-AGPL3
#
# This file is free software; as a special exception the author gives
# unlimited permission to copy and/or distribute it, with or without
# modifications, as long as this notice is preserved.
#
# This program is distributed in the hope that it will be useful, but
# WITHOUT ANY WARRANTY, to the extent permitted by law; without even the
# implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.

set(MYSQL_LIBRARY  "D:/dep/w_dep/mysql/lib/x64/libmysql.lib")
    
set(MYSQL_INCLUDE_DIR      "D:/dep/w_dep/mysql/include")

add_library(mysql STATIC IMPORTED GLOBAL)
 
set_target_properties(mysql
  PROPERTIES
    IMPORTED_LOCATION
      "${MYSQL_LIBRARY}"
    INTERFACE_INCLUDE_DIRECTORIES
      "${MYSQL_INCLUDE_DIR}")
