# regexTutorial_sf

## Table of Contents

--[Introduction](#introduction)

--[Start](#start)

--[Step1](#step1)

--[Step2](#step2)

--[Step3](#step3)

--[AboutMe](#aboutme)

##Introduction:
In this gist i will explain how to match an email address using a reqular expression, explaining the starter code of /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/.
I decided to use the email regex as it is among the most commonly used regular expressions as well as one that was very logical to me personally.

## Start:
The first character used is the /^ characters which marks the beginning of the input for the regex, whereas a $/ will mark the end.

## Step1:
The first paranthesis marks the first part of the email or the main body before the hosting site of the email,
inside we have square brackets that define all acceptable characters, which in this case is every lowercase letter of the alphabet defined as
a starting point of 'a' and and ending point of 'z', as well as every possible digit starting from 0 and ending at 9, the underscore character
is added immediately afterwards as it is also a viable character in this part of the input. The backslash specifically prevents the following character
(in this case '.' which is normally considered a "wildcard character" and to be completely honest I'm not entirely sure what that means) from being used as a special operation,
and is instead treated as another viable part of the input. Lastly a dash character is included in the acceptable input area, and the acceptable input area is closed out with an ending square bracket and followed by a plus sign which indicates that any number of character defined in the square brackets is acceptable, followed by an ending parenthesis which closes out this portion
of the email address.

## Step2:
Next an @ is placed as a hard requirement for the email address format as it defines the host site.
The host site input area is very similar to the main body input area but the first thing included is a \d, which in this case is shorthand for 0-9. This is another way to include arabic numerals as acceptable values. the we include a-z for all lowercase letters followed by \. to include periods and a - so that dashes are also allowed. This area is closed out with a plus sign to indicate any length, and following the closing parenthesis another \. is harcoded in. So now the acceptable email address looks something like "mainbody@website."

## Step3:
Which means that there is one more section to add which defines the type of host site. for the acceptable input area we are only allowing lowercase letters and periods. But this time instead of a plus sign we have {2,6}. What this does is set a specific length with a minimum of 2 and a maximum of 6. Finally the entire regular expression is closed out with $/.

## AboutMe:
Stefan Felbeck is a hot new face in the web development community. Originally beginning his Programming education in the game design course at the DigiPen Institute of Technology, he is now shifting gears towards web development to begin really learning the art and science of programming.

<a href="https://github.com/SFelbeck">You can find my GitHub here!</a>
