- Users of `#[reflect(Resource)]` will need to also implement/derive `FromReflect` (should already be the default).
- Users of `#[reflect(Resource)]` may now want to also add `FromWorld` to the list of reflected traits in case their `FromReflect` implementation may fail.
- Users of `ReflectResource` will now need to pass a `&TypeRegistry` to its `insert`, `apply_or_insert` and `copy` methods.