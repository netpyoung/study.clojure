# TODO


* https://github.com/taylorwood/clj.native-image
* https://github.com/Olical/cljs-test-runner
* https://github.com/cognitect-labs/test-runner


흠.. skia
https://github.com/HumbleUI/HumbleUI 를 써봐서 한번 간단한 테트리스로 만들어볼까?
 [Snake Game in Clojure and Skija](https://www.youtube.com/watch?v=KES-lKTq-3M)

* string interpolation
  - https://github.com/funcool/cuerdas/blob/master/src/cuerdas/core.cljc
  - https://funcool.github.io/cuerdas/latest/#interpolate
  - https://github.com/clojure/core.incubator

# 목차


목차는 저런식으로 해보면 어떨까.
* http://www.yes24.com/24/goods/66758183

* https://sarabander.github.io/sicp/html/index.xhtml#toc-Building-Abstractions-with-Procedures
SICP식으로 하면 너무 딱딱할것같다.
* 영어<->한국말은 sicp번역본처럼 어색하게(익숙치않게) 하지말자.


* helloworld
* in/out
  - 입력처리. stdin/stdout
* 가위 바위 보
  - 기본문법
  - number
  - boolean
  - string
  - 변수
  - if
* ??
  - list
  - vector
  - map
  - set
  - cond
* 별출력
  - doseq
  - for
  - loop
    - recur
  - defn - recur
  - reduce
     - reduced
* FizzBuzz
* file / io
* defprotocol / defrecord / deftype
* extend-type / extend-protocol
* exception handle
* lazy
* defmulti
* snake 지렁이
  - SDL
  - render loop
  - shape - triangle ...
* 패턴
  - command
  - seed
  - Actor Model
* 벽돌깨기
* 3D
  - OpenGL - jogl
* network
  - client & server
  - Http
    - ring
    - wrap - https://github.com/nberger/ring-logger/blob/master/src/ring/logger.clj
  - TCP/UDP
  - lockstep
* Serialization
  - datafy
  - json
  - edn
  - Protobuf
* embeded language . interpreter
* Macro
  - Dependence injection - https://github.com/kumarshantanu/dime



* monad
  - https://github.com/clojure/algo.monads
* AI
  - 길찾기 astar
* 미러 굴절
* 장기
  - alpha beta prunning
  - minimax



* guide
  - java version control - https://github.com/shyiko/jabba
  - fmt - https://github.com/kkinnear/zprint/blob/master/doc/graalvm.md
  - style: https://google.github.io/styleguide/lispguide.xml#Naming
  - lint
    - https://github.com/candid82/joker
  - documentation
  - test
    - bat-test
  - command line
    - https://github.com/clojure/tools.cli
  - command line
    - https://github.com/clojure/tools.cli
  - daemon
  - log

  - style
  - edu
    - defmacro / &form / &env
  - interface
    - https://github.com/clojure/clojure/tree/clojure-1.9.0/src/jvm/clojure/lang
    - I로 시작되는 interface
* Async
  - https://yobriefca.se/blog/2014/06/04/publish-and-subscribe-with-core-dot-asyncs-pub-and-sub/
  - https://github.com/clojure/core.async/wiki/Pub-Sub
  - async/pipeline
  - async/split
  - async/ toggle
  - https://github.com/johnboy14/core-async-sandbox


# TODO
* error handling - https://github.com/MichaelDrogalis/dire
* schema / spec
* profile
  - http://torsten.io/stdout/how-to-profile-clojure-code/




# TODO
* destructuring - https://github.com/jeaye/orchestra/blob/master/src/cljc/orchestra/detail.cljc


# SQL
https://github.com/jkk/honeysql

(-> (select :a [:b :bar] :c [:d :x])
    (from [:foo :quux])
    (where [:= :quux.a 1] [:< :bar 100])
    sql/format)
=> ["SELECT a, b AS bar, c, d AS x FROM foo quux WHERE (quux.a = ? AND bar < ?)" 1 100]


(fn [x] x.id == 10)

(-> table
     {:id :name}
     (q/filter qqq)
     (q/query))

https://stackoverflow.com/questions/3782970/how-can-i-display-the-definition-of-a-function-in-clojure-at-the-repl


----------------------

https://github.com/metabase/metabase

[metabase.api.common :refer [*current-user-id* defendpoint define-routes]]

-------------------


https://bitbucket.org/cuchaz/jfxgl/src

In to the byte code


https://github.com/nasser/magic



#
infix / prefix

Math

javafx api designed for fit on java
fluent api

so it isn't suitable not suitable for clojure
need some other way(need to change mindset)




ClojureCRL
Symbolic MSIL bytecode generation for ClojureCLR
https://github.com/nasser/mage
https://www.youtube.com/watch?v=eDad1pvwX34




asm helloworld
https://gongon95.wordpress.com/2015/07/13/asm%ec%9c%bc%eb%a1%9c-java-class-file-%ec%83%9d%ec%84%b1%ed%95%98%ea%b8%b0/

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------





-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
code-gen
JSR 223
https://en.wikipedia.org/wiki/Scripting_for_the_Java_Platform
Scripting for the Java Platform is a framework for embedding scripts into Java source code.
Scripting for the Java Platform was developed under the Java Community Process as JSR 223. The final release of JSR 223 happened on December 11, 2006. The specification, however, was withdrawn later on December 13, 2016 after a Maintenance Review Ballot,[1] where it was decided that this functionality would be included as an integral part of Java 9 and onward.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------










-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


etc - library
=====================
boot


[
 [org.clojure/clojure "1.9.0"]
 [swiss-arrows "1.0.0"]
   https://github.com/rplevy/swiss-arrows

(-<> 2
(* <> 5)
(vector 1 2 <> 3 4))
=> [1 2 10 3 4]

 [camel-snake-kebab "0.4.0"]
  https://github.com/qerub/camel-snake-kebab
(->camelCase 'flux-capacitor)
; => 'fluxCapacitor

(->SCREAMING_SNAKE_CASE "I am constant")
; => "I_AM_CONSTANT"


 [com.taoensso/timbre "4.7.4" :exclusions [com.taoensso/carmine]]
  https://github.com/ptaoussanis/timbre
(ns my-clj-ns ; Clojure namespace
(:require
[taoensso.timbre :as timbre
:refer [log trace debug info warn error fatal report
logf tracef debugf infof warnf errorf fatalf reportf
spy get-env]]))

 -- https://github.com/ptaoussanis/carmine
   Redis client and message queue for Clojure https://www.taoensso.com

 [net.openhft/compiler "2.3.0"]
   https://github.com/OpenHFT/Java-Runtime-Compiler
 [org.ow2.asm/asm "6.0"]
 [org.ow2.asm/asm-util "6.0"]
https://gitlab.ow2.org/asm/asm - https://asm.ow2.io/
 [clojure-jsr-223 "0.1.0"]
]

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


TODO



http://nils-blum-oeste.net/javafx-style-using-clojure-fn-fx-garden-desktop-application-design/
http://nils-blum-oeste.net/functional-gui-programming-with-clojure-and-javafx-meet-halgarifn-fx/


string css
https://stackoverflow.com/questions/24704515/in-javafx-8-can-i-provide-a-stylesheet-from-a-string

garden

Scoop — scoop bucket add extras && scoop install boot-clj


# King
https://www.defold.com/editor-two/

https://techblog.king.com/javafx-used-build-desktop-application/


# tracking
http://fxexperience.com/




=================
Boot
System

https://github.com/oakes/Nightcode


	*
Clojurescript

		*
https://github.com/metametadata/carry
		*
https://github.com/Gonzih/cljs-electron



------------------------------
https://github.com/athos/nrepl-revolver

http://gekko.tistory.com/138
midi ?

graphic = libjgl
https://javadoc.lwjgl.org/org/lwjgl/nuklear/Nuklear.html



ingame gui?
https://github.com/vurtun/nuklear


tool gui - javafx



test
https://github.com/rogerallen/hello_lwjgl


sound
https://docs.oracle.com/javase/tutorial/sound/overview-MIDI.html
https://docs.oracle.com/javase/tutorial/sound/MIDI-synth.html

sound - clojure
http://blog.djy.io/making-midi-sound-awesome-in-a-clojure-program/

sound - dependency too heavy??
http://mad.emotionull.com/

# todo research
http://www.l33tlabs.com/
LWJGL: Pong Game #2 GUI Setup - YouTube

https://www.youtube.com/watch?v=duDO24VNtK4

--------------------
https://github.com/clojure-emacs/cider/blob/master/doc/debugging.md
	* https://electron.atom.io/
	* https://www.youtube.com/watch?v=tBnu2JmK4p0

https://github.com/danielsz/system


# meetup api
https://secure.meetup.com/meetup_api/console/?path=/:urlname/events

https://api.meetup.com/clojure-tokyo/events?&sign=true&photo-host=public&page=20

— need authorize api


# GITHUB API
https://stackoverflow.com/questions/28391901/using-the-github-api-create-git-pull-request-without-checking-out-the-code


# 검증 - 특정폴더
https://github.com/clj-jgit/clj-jgit

# travis-lint
gem install travis-lint


# travis ci
https://docs.travis-ci.com/user/customizing-the-build/#Building-Specific-Branches
https://docs.travis-ci.com/user/pull-requests/


# gitter
<iframe src="https://gitter.im/clojure_tokyo/Lobby/~embed">
react iframe
https://okjungsoo.wordpress.com/2017/01/26/iframe-%EB%AC%B8%EC%84%9C-%EB%86%92%EC%9D%B4-%EA%B0%80%EC%A0%B8%EC%99%80%EC%84%9C-%EC%97%85%EB%8D%B0%EC%9D%B4%ED%8A%B8-%ED%95%98%EA%B8%B0/



# youtube player list
<iframe width="560" height="315" src="http://www.youtube.com/embed/T0Jqdjbed40?playlist=SyoA4LXQco4,6l6PPvUhR4c" frameborder="0" allowfullscreen></iframe>
<iframe width="560" height="315" src="http://www.youtube.com/embed?listType=playlist&list=FLz97F7dMxBNOfGYu3rx8aCw" frameborder="0" allowfullscreen></iframe>

# debuging
https://github.com/binaryage/cljs-devtools
https://github.com/binaryage/cljs-devtools/blob/master/docs/installation.md




https://github.com/FastLabs/boot2cloj
https://github.com/ahammel/arpad
https://github.com/hellonico/maths


https://github.com/search?l=clojure&p=2&q=line-seq+chan&type=Code&utf8=%E2%9C%93
https://github.com/danielsz/system-advanced-example



Clojure for functional testing of Mobile and Web apps by Mayur @ Selenium Conf 2014
https://www.youtube.com/watch?v=G-fjpO6nYPQ

https://www.youtube.com/watch?v=inPK2VXdV_w
분석하기.


decopmiler
dll
https://www.jetbrains.com/decompiler/

jar
http://jd.benow.ca/





emacs - lisp setting
http://unipro.tistory.com/226?category=502322


clojure
*data-readers* - https://clojure.org/reference/reader#_extensible_data_notation_edn

https://www.slideshare.net/KentOhashi/spectacular-future-with-clojurespec

http://gigasquidsoftware.com/blog/2016/07/18/genetic-programming-with-clojure-dot-spec/

racket
http://slides.com/ronie/racket-beyond-clojure#/8

timeline
https://en.wikipedia.org/wiki/Lisp_(programming_language)#Timeline

animation optimize
http://www.strichnet.com/how-to-improve-the-performance-of-unity3d-animations/


# gitlabpage
https://github.com/cryogen-project/cryogen

https://github.com/hashobject/perun


clojurescript


https://www.staticgen.com/

https://about.gitlab.com/2016/04/07/gitlab-pages-setup/


# testing
https://github.com/fukamachi/rove




jogl - Java™ Binding for the OpenGL® API
https://jogamp.org/jogl/www/

boot-protobuf
https://github.com/aJchemist/boot-protobuf


  :codox             {:sources                   ["src/clj"]
                      :output-dir                "target/doc/api"
                      :exclude                   [internal]
                      :src-dir-uri               "http://github.com/relevance/defold/blob/clojure-sceneed"
                      :src-linenum-anchor-prefix "L"
                      :defaults                  {:doc/format :markdown}}

                     [at.bestsolution.eclipse/org.eclipse.fx.code.editor.fx "2.2.0"]
https://logback.qos.ch/

                     [joda-time/joda-time                         "2.9.2"]


    [commons-io/commons-io                       "2.4"]
                     [commons-configuration/commons-configuration "1.10"
                      :exclusions [commons-logging/commons-logging]] ; commons-configuration -> 1.1.1, amazonica -> 1.2
                     [commons-codec/commons-codec                 "1.10"]



https://github.com/projectodd/shimdandy - A shim wrapping Clojure's runtime to facilitate multiple Clojure runtimes in the same JVM.
                     [org.projectodd.shimdandy/shimdandy-api      "1.2.0"]
                     [org.projectodd.shimdandy/shimdandy-impl     "1.2.0"]
