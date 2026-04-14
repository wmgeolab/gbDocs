# Generalization vs. Fidelity

This page explains how to balance **generalization** (simplifying geometry) and **fidelity** (preserving the original detail) when working with boundary data.

The goal is to maintain accuracy while avoiding unnecessary complexity.

---

## Definitions

- **Fidelity:** Preserving the original shape and detail of the source data  
- **Generalization:** Reducing detail to simplify geometry

---

## Guiding Principle

> Prioritize **fidelity to the source data**.  
> Only generalize when necessary and without altering meaning.

---

## When to Preserve Fidelity

Maintain the original geometry when:

- The source data is high quality
- Boundaries contain important detail (e.g., coastlines, rivers)
- Simplification would change the shape or meaning of the boundary

---

## When Generalization Is Acceptable

Generalization may be appropriate when:

- Geometry is excessively complex (very high vertex count)
- Data causes performance issues
- Minor smoothing does not change boundary meaning

---

## What to Avoid

- Over-simplifying boundaries
- Removing important geographic features
- Altering official boundaries
- Editing beyond what the source supports

---

## Common Issues

### Over-Generalization

**Issue:**  
Boundaries lose important detail and appear unrealistic.

**Fix:**  
- Revert to the original source if possible  
- Use a higher-quality dataset  

---

### Excessive Detail

**Issue:**  
Too many vertices create unnecessary complexity.

**Fix:**  
- Simplify carefully while preserving shape  

→ See: [Editing Geometries](../40-qgis-user-manual/editing-geometries.md)

---

## Best Practices

- Match the **level of detail across the dataset**
- Keep boundaries **consistent between neighboring regions**
- Avoid mixing highly detailed and highly simplified features
- Always compare edits to the original source

---

## Validation

Before submission:

- Inspect boundaries at multiple zoom levels  
- Ensure shapes look natural and consistent  
- Confirm no important features were lost  

→ See: [Topology and Validity](../40-qgis-user-manual/topology-and-validity.md)

---

## Summary

- Favor fidelity over unnecessary generalization  
- Simplify only when it does not impact accuracy  
- Maintain consistent detail across the dataset  

Striking the right balance ensures data is both accurate and usable.
