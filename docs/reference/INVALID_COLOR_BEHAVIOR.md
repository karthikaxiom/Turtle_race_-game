# Invalid color behavior

The input dialog accepts text without a validation step against the configured color list. An unsupported color therefore does not prevent the race from starting; it simply fails the final equality comparison unless it matches the winner color.