def sort_by_typing_handedness(words):

    lenwords = [len(i) for i in words]
    lh = [int(y) if y.isdigit() else y for y in [x.replace('u', '').replace('i', '').replace('o', '').replace('p', '').replace('j', '').replace('k', '').replace('l', '').replace('n', '').replace('m', '') for x in words]]
    lenlh = [len(i) for i in lh]
    score = [lenlh - (lenwords - lenlh) for lenwords, lenlh in zip(lenwords, lenlh)]    
    zl = zip(words, score)
    dzl = dict(zl)
    items = [(v, k) for k, v in dzl.items()]
    items.sort()
    items.reverse()
    items = [(k, v) for v, k in items]
    sortitems = sorted(items, key=lambda tup: (-tup[1], tup[0]))
    result = [(v) for v, k in sortitems]
    return result
