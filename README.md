# egglog-smt

## SMT Final Project Reproduction

To reproduce the SMT final project results, you can run the following commands:

```bash
# Or any other way to install the z3 CLI command
brew install z3
# install rust https://rust-lang.org/tools/install/
git clone git@github.com:RockingMat/egglog-smt.git
cd egglog-smt

# To run the smt lib examples:
cargo run tests/smt-bool.egg
cargo run tests/smt-real.egg
cargo run tests/smt-bitvec.egg

# To run the SMT calculus example:
cargo run tests/smt-math.egg

# To run the factoring example:
cargo run tests/polynomial/factor-rat.egg

# To run the polynomial benchmarks:
cd egglog-smt/tests/polynomials/benchmark
python3 benchmark.py
python3 rearranging_benchmark.py
rm -rf temp_tests
```

Prepending any `cargo` command with `env SMT_DEBUG=1` will provide additional under-the-hood information about solver calls.
