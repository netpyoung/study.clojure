IKeywordLookup{
ILookupThunk getLookupThunk(Keyword k);
}

ILookup{
Object valAt(Object key);
Object valAt(Object key, Object notFound);
}

ITransientCollection{
ITransientCollection conj(Object val);
IPersistentCollection persistent();
}

ITransientAssociative extends ITransientCollection, ILookup{
ITransientAssociative assoc(Object key, Object val);
}

ITransientAssociative2 extends ITransientAssociative {
boolean containsKey(Object key);
IMapEntry entryAt(Object key);
}
