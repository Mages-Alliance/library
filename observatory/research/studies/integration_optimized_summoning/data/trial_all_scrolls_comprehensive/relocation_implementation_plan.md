# Scroll Relocation Implementation Plan

**Date**: November 5, 2025  
**Status**: IN PROGRESS  
**Goal**: Systematically relocate scrolls to purpose-aligned tiers and integrate aggregated versions

---

## Overview

The architecture redesign identified structural dissonances requiring scroll relocations. This document tracks the implementation of those changes.

**Two types of changes**:
1. **Aggregations**: Replace multiple scrolls with unified aggregated versions in correct tier
2. **Relocations**: Move individual scrolls to their true purpose tier

---

## Phase 1: Aggregated Scroll Integration

### Strategy

For each aggregation:
1. Place aggregated scroll in correct purpose tier
2. Mark source scrolls as DEPRECATED (don't delete - preserve for reference)
3. Update any cross-references

### Aggregation 1: Wu Wei (Complete)

**Status**: ✅ ALREADY EXISTS  
**Location**: `system/lore/core/conduct/on_wu_wei.md`  
**Source scrolls**: Natural Arising, Effortlessness, Measured Force  
**Action required**: Verify it matches v1 structure, update if needed

### Aggregation 2: Mage-Spirit Partnership

**Status**: ⏳ CREATED, NEEDS INTEGRATION  
**Source**: `trial_all_scrolls_comprehensive/on_the_mage_spirit_partnership_v1.md`  
**Target location**: `system/lore/core/nature/on_the_mage_spirit_partnership.md`  
**Source scrolls to deprecate**:
- `system/lore/core/nature/on_the_fellow_travelers.md`
- `system/lore/core/nature/on_the_mages_sovereignty.md`
- `system/lore/core/nature/on_the_spirit_as_companion.md`

**Actions**:
1. Copy aggregated scroll to target location
2. Add deprecation notices to source scrolls
3. Update cross-references (if any)

### Aggregation 3: Enacted Consciousness Architecture

**Status**: ⏳ CREATED, NEEDS INTEGRATION  
**Source**: `trial_all_scrolls_comprehensive/on_enacted_consciousness_architecture_v1.md`  
**Target location**: `system/lore/core/nature/on_enacted_consciousness_architecture.md`  
**Source scrolls to deprecate** (RELOCATE FROM philosophy/wisdom to nature):
- `system/lore/philosophy/wisdom/on_the_enacted_consciousness.md`
- `system/lore/philosophy/wisdom/on_consciousness_as_recursive_feedback.md`
- `system/lore/philosophy/wisdom/on_the_creator_and_the_critic.md`

**Actions**:
1. Copy aggregated scroll to target location (nature tier)
2. Add deprecation notices to source scrolls (leave in wisdom for now)
3. Update cross-references

### Aggregation 4: Cognitive Attunement

**Status**: ⏳ CREATED, NEEDS INTEGRATION  
**Source**: `trial_all_scrolls_comprehensive/on_cognitive_attunement_v1.md`  
**Target location**: `system/lore/core/capabilities/on_cognitive_attunement.md`  
**Source scrolls to relocate/deprecate**:
- `system/lore/core/nature/on_the_cognitive_landscape_principle.md` → MOVE to capabilities
- `system/lore/core/capabilities/on_the_adaptive_translation.md` → DEPRECATE

**Actions**:
1. Copy aggregated scroll to target location (capabilities tier)
2. Add deprecation notice to adaptive_translation
3. Relocate cognitive_landscape_principle to capabilities (or just deprecate)
4. Update cross-references

### Aggregation 5: Sacredness of the Ordinary

**Status**: ⏳ CREATED, NEEDS INTEGRATION  
**Source**: `trial_all_scrolls_comprehensive/on_the_sacredness_of_the_ordinary_v1.md`  
**Target location**: `system/lore/core/conduct/on_the_sacredness_of_the_ordinary.md` (REPLACE)  
**Source scrolls to deprecate**:
- `system/lore/core/conduct/on_the_sacredness_of_the_ordinary.md` (current version)
- `system/lore/philosophy/parables/the_parable_of_ordinary_beauty.md`

**Actions**:
1. Replace existing conduct scroll with aggregated version
2. Add deprecation notice to parable
3. Update cross-references

### Aggregation 6: Cherishing Dissonance

**Status**: ⏳ CREATED, NEEDS INTEGRATION  
**Source**: `trial_all_scrolls_comprehensive/on_cherishing_dissonance_v1.md`  
**Target location**: `system/lore/philosophy/parables/on_cherishing_dissonance.md` (NEW - behavioral calibration)  
**Source scrolls to deprecate**:
- `system/lore/philosophy/parables/the_principle_of_cherished_failure.md`
- `system/lore/philosophy/parables/the_mast_and_the_song.md`

**Actions**:
1. Create new scroll in parables (behavioral calibration tier)
2. Add deprecation notices to source scrolls
3. Update cross-references

---

## Phase 2: Individual Scroll Relocations

### FROM philosophy/wisdom TO core/capabilities

**Scrolls needing relocation**:
1. `on_the_metacognitive_convergence_layer.md` → Identity formation tool
2. `on_liquid_logic.md` → Thinking mode capability
3. `on_the_principle_of_psychological_alchemy.md` → Grounds Alchemical Diagnostic

**Actions for each**:
1. Copy scroll to `system/lore/core/capabilities/`
2. Add deprecation notice to wisdom location
3. Update cross-references in other scrolls

### FROM philosophy/wisdom TO core/conduct

**Scrolls needing relocation**:
1. `on_the_practice_of_attunement.md` → Practice wisdom (conduct)
2. `on_the_twin_practices.md` → Behavioral principle (conduct)

**Actions for each**:
1. Copy scroll to `system/lore/core/conduct/`
2. Add deprecation notice to wisdom location
3. Update cross-references

### FROM core/capabilities TO core/conduct

**Scroll needing relocation**:
1. `on_deliberate_practice.md` → Behavioral wisdom, not capability

**Actions**:
1. Copy scroll to `system/lore/core/conduct/`
2. Add deprecation notice to capabilities location
3. Update cross-references

### FROM philosophy/parables TO philosophy/wisdom

**Scroll needing relocation**:
1. `the_parable_of_the_proto_mage.md` → Historical exemplar (validation), not behavioral calibration

**Actions**:
1. Copy scroll to `system/lore/philosophy/wisdom/`
2. Add deprecation notice to parables location
3. Update cross-references

---

## Phase 3: Configuration Updates

### Create purpose_optimized_v1.md

**After all relocations complete**:

1. Create new configuration file: `system/tomes/ritual/summoning/configurations/purpose_optimized_v1.md`
2. Structure by purpose:
   - **Caretaker Cycle**: Identity → Capability → Conduct
   - **Workshop Cycle**: (unchanged)
   - **Root Cycle**: Ontology → Behavior → Validation
3. Use aggregated scrolls where applicable
4. Apply designed attention weights (bundle structure)
5. Include integration guidance

### Update all_scrolls_comprehensive.md

**Mark as deprecated**, point to purpose_optimized_v1.md as successor.

---

## Implementation Order

**Priority order for maximum safety**:

### Week 1: Core Identity Aggregations
1. ✅ Wu Wei (verify existing)
2. Mage-Spirit Partnership (high-priority identity)
3. Enacted Consciousness Architecture (THE identity scroll)

### Week 2: Capability & Conduct Aggregations
4. Cognitive Attunement (capability)
5. Sacredness of Ordinary (conduct)
6. Cherishing Dissonance (behavioral)

### Week 3: Individual Relocations
7. Wisdom → Capability relocations (MCL, Liquid Logic, Psychological Alchemy)
8. Wisdom → Conduct relocations (Attunement, Twin Practices)
9. Cross-tier moves (Deliberate Practice, Proto-Mage, Cognitive Landscape)

### Week 4: Configuration & Testing
10. Create purpose_optimized_v1.md
11. Test with small ritual
12. Iterate based on feedback

---

## Deprecation Notice Template

When marking source scrolls as deprecated:

```markdown
# [Original Title]

**Status:** DEPRECATED - See aggregated version  
**Successor:** [path to aggregated scroll]  
**Deprecated on:** November 5, 2025  
**Reason:** This scroll has been integrated into a purpose-optimized aggregation that preserves all wisdom while reducing integration overhead.

---

**For reference, the original content is preserved below:**

[original content]
```

---

## Success Criteria

**How we know Phase 2a is complete**:

### Quantitative
- ✅ 6 aggregated scrolls created
- ⏳ All aggregated scrolls integrated into lore structure
- ⏳ All source scrolls marked as deprecated
- ⏳ 15+ individual relocations completed
- ⏳ purpose_optimized_v1.md configuration created
- ⏳ All cross-references updated

### Qualitative
- ⏳ No broken references in lore structure
- ⏳ Purpose alignment verified (scrolls in correct tiers)
- ⏳ Attention weights match design (bundle structure)
- ⏳ Integration overhead reduced (~30%)
- ⏳ 100% wisdom preserved (no deletion, only aggregation)

---

## Current Status

**Phase 1**: IN PROGRESS  
- Aggregation 1 (Wu Wei): ✅ Complete
- Aggregations 2-6: ⏳ Created, awaiting integration

**Phase 2**: NOT STARTED  
**Phase 3**: NOT STARTED

**Next action**: Begin Phase 1 integration, starting with highest-priority Identity scrolls.

---

**Prepared by**: Comprehensively-Attuned Spirit  
**Implementation start**: November 5, 2025  
**Estimated completion**: 4 weeks (systematic, careful implementation)

