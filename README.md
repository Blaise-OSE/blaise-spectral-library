# blaise-spectral-library

Community-contributed Raman spectral data library for the Blaise Raman spectrometer platform
— part of the [Blaise OSE](https://github.com/Blaise-OSE).

Every validated spectrum contributed by [Blaise xTECH Challenge](https://support.forwardedge.ai/en/?q=XTECH)
teams expands the range of substances the platform's AI models can detect. Contribution is a
condition of advancement through the competition — the OSE targets 50,000 validated spectra
by month 36.

## Status

🚧 This repository currently contains documentation only. Spectral contribution opens with
the xTECH Challenge on **August 1, 2026**.

## Data format

Accepted spectra are stored in open **HDF5** format with:

- Standardized metadata schemas
- Unique identifiers enabling full provenance tracing
- No personally identifiable information, by design

## Ingestion pipeline

1. **Automated ingestion** — checks file format compliance, metadata completeness,
   wavenumber calibration alignment, and minimum signal quality thresholds.
2. **Working group data quality review** — human reviewers assess biological/chemical
   plausibility and assign confidence scores.
3. **Cross-validation** — new spectra are compared against existing library entries to
   detect duplicates, flag anomalies, and confirm classification consistency before
   influencing AI model training.

Submissions that fail automated acceptance criteria are returned with specific remediation
guidance rather than silently rejected.

## Quality criteria

Published spectral acceptance criteria define, per molecular category:

- Minimum signal-to-noise ratios
- Wavenumber accuracy tolerances
- Replicate consistency thresholds

## Security and privacy

- Spectral files contain no personally identifiable information by design.
- Contributor account data is stored separately from spectral submissions and collected
  under explicit consent (GDPR-aligned).
- Contributors may request pseudonymous attribution.
- Access to high-harm-potential compound data is restricted to verified institutional
  accounts as part of dual-use risk mitigation.

## Related repositories

- [blaise-sdk](https://github.com/Blaise-OSE/blaise-sdk) — core AI SDK
- [blaise-applications](https://github.com/Blaise-OSE/blaise-applications) — published competitor applications
- [blaise-docs](https://github.com/Blaise-OSE/blaise-docs) — technical documentation and integration guides

## License

Creative Commons Attribution 4.0 International (CC-BY 4.0) — see [LICENSE](https://github.com/Blaise-OSE/blaise-spectral-library/blob/main/LICENSE).
