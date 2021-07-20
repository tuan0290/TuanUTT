#!/bin/bash
if [ -e $1 ]
then
rm -r $1
echo "Delete!"
else
touch $1
echo "Create!"
fi
