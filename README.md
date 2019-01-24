# study.clojure


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


* Emacs
  - 필수로 해야할까?
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
