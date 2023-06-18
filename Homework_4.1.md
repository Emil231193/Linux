#!/bin/bash
if [ -d $1 ]
then
echo "Got it!"
for file in $1/*
do
if [[ $file == *.bak ]] || [[ $file == *.tmp ]] || [[ $file == *.backup ]]
then
rm $file
fi
done
echo "Done"
else
echo "Directory does not exist"
fi
