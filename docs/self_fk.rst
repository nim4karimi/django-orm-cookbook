How to include a self-referencing Foreignkey in a model
========================================================================

Self-referencing fk(recursive relationship)  works similar to what we do for One to Many relationships. But as the name suggests, the model references itself. Self reference Foreignkey can be achived in two ways: ::

    class Parent(models.Model):
        parent_ref = models.ForeignKey('self', on_delete=models.CASCADE))

                   // OR

    class Parent(models.Model):
        parent_ref = models.ForeignKey("Parent", on_delete=models.CASCADE))

