``` clojure
(defn grouping-increase
  "
  ;; (grouping-increase 3 [1 2 3 1 2 3 4 1 2 1 2 3 4 5])
  ;;=> [[1 2 3] [1 2 3 4] [1 2 3 4 5]]
  "
  [cnt coll]
  (loop [[fst & rst] (map vector coll (conj (vec (rest coll)) (first coll))), coll [], acc []]
    (if-not fst
      acc
      (let [[a b] fst, coll (conj coll a)]
        (if (= (inc a) b)
          (recur rst coll acc)
          (recur rst [] (if (< (count coll) cnt) acc (conj acc coll))))))))


(defn alter-for
  "
  ;; (= (alter-for [[1 2] [3 4]])
  ;;    (for [x [1 2] y [3 4]] [x y]))
  "
  [coll]
  (loop [[fst & rst] coll, acc []]
    (if-not fst
      (let [[fst & rst] acc]
        (apply mapv vector (into [fst] (map cycle rst))))
      (let [cnt (reduce * (map count rst))]
        (if (zero? cnt)
          (recur rst (conj acc fst))
          (recur rst (conj acc (mapcat #(repeat cnt %) fst))))))))
```
