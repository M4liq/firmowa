On Windows

export:
winpty docker exec -it <container_id> mysqldump --all-databases -uwordpress -p"wordpress" --result-file=dumps/full-dump.sql

import:
winpty docker exec -it <container_id> bin/bash
mysql -uwordpress -p"wordpress" < dumps/full-dump.sql

