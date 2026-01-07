import java.util.ArrayList;
import java.util.Comparator;
import java.util.HashSet;
import java.util.List;
import java.util.Set;

record Pair(int val1, int val2) {

    @Override
    public boolean equals(Object o) {
        if (this == o) return true;
        if (!(o instanceof Pair other)) return false;
        return (this.val1 + this.val2) == (other.val1 + other.val2);
    }

    @Override
    public int hashCode() {
        return Integer.hashCode(val1 + val2);
    }
}

class Container {
    
    private final Set<Pair> pairs;

    public Container(List<Pair> list) {
        this.pairs = new HashSet<>();
        if (list != null) {
            this.pairs.addAll(list);
        }
    }

    public List<Integer> process() {
        List<Integer> result = new ArrayList<>();

        for (Pair p : pairs) {
            long product = (long) p.val1() * (long) p.val2();
            if (product >= -150 && product < 150) {
                result.add((int) product);
            }
        }

        result.sort(Comparator.reverseOrder());
        return result;
    }

    public void removeOnCondition() {
        pairs.removeIf(p -> (p.val1() + p.val2()) < 0);
    }
}
