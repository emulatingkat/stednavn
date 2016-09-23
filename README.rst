Stednavn
========

.. code:: bash

    curl "http://runeberg.org/download.pl?mode=ocrtext&work=bentbille" > bentbille.txt
    python -m stednavn bentbille.txt

In Python:

    >>> from stednavn import Stednavn
    >>> stednavn = Stednavn()
    >>> stednavn.extract_placenames_from_string(u'Lyngby Hovedgade er i Kongens Lyngby ikke i København eller Ørum.')
    [u'Lyngby Hovedgade', u'Kongens Lyngby', u'K\xf8benhavn', u'\xd8rum']
