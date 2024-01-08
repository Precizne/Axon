case "$1" in

# ---------------Create---------------
   "create")
      mkdir $2;
      cd $2;
      case "$3" in
      #-----C++-----
         "cpp")
            touch main.cpp;
            touch build.sh;
            chmod +x build.sh;
            echo "echo \"<<-COMPILING->>\";
case \$1 in
   a)
      g++ -O1 -Wall -fuse-ld=lld -std=c++20 -fsanitize=address -fno-omit-frame-pointer main.cpp;;
   m)
      g++ -O1 -Wall -fuse-ld=lld -std=c++20 -fsanitize=memory -fPIE -pie -fno-omit-frame-pointer -fno-optimize-sibling-calls -g main.cpp;;
   t)
      g++ -O1 -Wall -fuse-ld=lld -std=c++20 -fsanitize=thread -fPIE -pie -g main.cpp;;
   l)
      g++ -O1 -Wall -fuse-ld=lld -std=c++20 -fsanitize=leak main.cpp;;
   u)
      g++ -O1 -Wall -fuse-ld=lld -std=c++20 -fsanitize=undefined main.cpp;;
   *)
      g++ -Ofast -Wall -fuse-ld=lld -std=c++20 main.cpp;;
esac
echo \"<<-EXECUTING->>\";
./a.out;" > build.sh;;
         
      #-----Java-----
         "java")
            touch Main.java;
            touch build.sh;
            chmod +x build.sh;
            echo "echo \"<<-COMPILING->>\";
javac Main.java;
echo \"<<-EXECUTING->>\";
java Main;" > build.sh;;

      #-----Python-----
         "python")
            touch main.py;
            touch build.sh;
            chmod +x build.sh;
            echo "echo \"<<-EXECUTING->>\";
python main.py;" > build.sh;;

      #-----Invalid-----
         *)
            echo "Invalid Argument";;

      esac;;

# ---------------Build--------------- 
   "build")
      ./build.sh $2;;

esac
