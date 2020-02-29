
case $# in 
0)	echo 'Bad usage: argument missing' 1>&2; exit 1 ;;
1)  echo "Need challenge's number sorry, bye bye..." 1>&2; exit 1 ;;
*)  numb=$2 ;;
esac

wget $1
name="`ls -t | tail -1`"
echo $name
var="challenge_$numb.gz"

case $name in 
challenge_$numb.gz) echo $name ;;
*)	echo 'Wrong wrong wrong' 1>&2; exit 1 ;;
esac


tar xzfv $var
cd image/challenge/
mv challenge ../../ && cd ../../
chmod +x challenge
rm -r image && rm $var


