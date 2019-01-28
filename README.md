This repository contains a [Minerva][1] core compiled from [nMigen][2] to Verilog.
It has been checked out at `45b8034a3c0d65339173274916230809de6fab15` and built with the following configuration:

```
| Parameter         | Value        |
| ----------------- | ------------ |
| `reset_address`   | `0x00000000` |
| `with_icache`     | `True`       |
| `icache_nb_ways`  | `1`          |
| `icache_nb_lines` | `256`        |
| `icache_nb_words` | `8`          |
| `icache_base`     | `0x00000000` |
| `icache_limit`    | `0x80000000` |
| `with_dcache`     | `True`       |
| `dcache_nb_ways`  | `1`          |
| `dcache_nb_lines` | `256`        |
| `dcache_nb_words` | `8`          |
| `dcache_base`     | `0x00000000` |
| `dcache_limit`    | `0x80000000` |

```

nMigen currently propagates a lot of unneeded inputs to the toplevel. To use Minerva, you only need to wire the following ports to `minerva_cpu`:

* `clk`
* `rst`
* `ibus_*`
* `dbus_*`
* `external_interrupt`

[1]: https://github.com/lambdaconcept/minerva/
[2]: https://github.com/m-labs/nmigen/
