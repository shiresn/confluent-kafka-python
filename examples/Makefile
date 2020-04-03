WORK_DIR:=$(strip $(shell dirname $(realpath $(lastword $(MAKEFILE_LIST)))))
SRC_DIR?=$(WORK_DIR)
TARGET_DIR?=$(WORK_DIR)

PROTOS := user.proto

user_pb2.py: user.proto
	protoc -I=$(SRC_DIR) --python_out=$(TARGET_DIR) $(SRC_DIR)/user.proto;

clean:
	rm -f $(TARGET_DIR)/*_pb2.py
