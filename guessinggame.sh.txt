#!/usr/bin/env bash


{
    true_ans=$(ls -l |grep "^-"|wc -l)
    echo "Hey Guys..!! Let's Play a Guessing Game..."
    while true;
    do
        echo "Please... Enter your guess:"
        read  number
        if [ $number -lt $true_ans ]
        then
            echo "Oops!!! Your guess is too Low !!"
        elif [ $number -gt $true_ans ]
        then
            echo "Oops!!! Your guess is too High!!"
        else
            echo "Congratulation!!! Your Right!!"
        break;
        fi
    done
}

