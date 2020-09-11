# Bash Scripting

#!/bin/bash

## Array Example

declare -a tokens=( "one" "two" "three" )

echo "arry contents: ${tokens[@]}"

## adding elements

tokens+=( "four" )

## deleting element

unset 'tokens[2]'

## Looping through array

for token in "${tokens[@]}"; do
        echo "  element: $token"
done

## Number of elements in array

echo "count = ${#tokens[@]}"

echo -e "\n* Map "

# Maps

declare -A amap=( ["one"]="1" ["two"]="2" )

## add element

amap["three"]="3"

## keys

echo -e "\n** Keys of Map"
echo "keys: ${!amap[@]}"

## values

echo -e "\n** Values of Map"

echo "values: ${amap[@]}"

## loop through map

echo -e "\n** Looping Map"

for name in "${!amap[@]}"; do
        printf "%-5s -> %-5s\n" "$name" "${amap[$name]}";
done


# Read Command Output line by line to while loop

echo -e "\n** cat first 5 lines of this file line by line"

while IFS= read -r line; do
        echo "->$line";
done < <(cat $0 |head -n 5)
